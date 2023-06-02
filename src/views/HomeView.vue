<template>
    <v-app id="home">
        <NavBar/>
        <v-container fluid>
            <div class="head">
                <v-row>
                    <v-col cols="5">
                        <div style="position:relative" class="mt-16">
                            <h1 class="text-grey">Hello,</h1>
                            <h1 class="text-white">I'm Ziaur Rahman</h1>
                            <span class="text-grey">Full Stack Developer</span><br />
                            <v-btn tile dark class="text-yellow mt-8" variant="outlined">Contact me</v-btn>
                        </div>
                    </v-col>
                    <v-col cols="2">
                        <div style="position:absolute; z-index: 9999; bottom: 0; margin-left: auto; mergin-right: auto; left: 0; right: 0; text-align: center;">
                            <v-icon>fas fa-angle-double-down</v-icon>
                        </div>
                    </v-col>
                    <v-col cols="5">
                        <div style="position:relative; z-index: 9999;" class="mt-16">
                            <v-img src="profile_pic.png" contain max-height="300"></v-img>
                        </div>
                    </v-col>
                </v-row>
            </div>
            <v-col cols="12" class="mt-16" id="about">
                <div>
                    <v-row>
                        <v-col cols="12" sm="6">
                            <div class="egg">
                                <v-img src="wow.png" contain max-height="300"></v-img>
                            </div>
                        </v-col>
                        <v-col cols="12" sm="6">
                            <h5 class="mt-16">About me</h5>
                            <div style="width: 120px">
                                <v-slider v-model="slider2" color="yellow" thumb-label="always"></v-slider>
                            </div>
                            <h4 class="mt-n4">I Am a Creative Full Stack Developer</h4>
                            <h4> And Devops Engineer</h4>
                            <p class="text-grey">
                                I am a full stack developer and devops engineer. I can develop any kind of web application. I have 7+ years of experience in web development. I have worked with many clients and companies. I have worked with many technologies like Laravel, Vuejs, Vuetifyjs, MongoDB, MySQL, PostgreSQL, Redis, Docker, Kubernetes, AWS, GCP, Digital Ocean, Linode, etc.
                            </p>
                            <br />
                            <p class="text-grey">
                                I have developed many web applications like CRM, ERP, POS, HRM, Accounting, Inventory, Fintech solutions etc. I have also developed many websites like e-commerce, blog, portfolio, etc. I have also developed many APIs for mobile applications. I have also developed many mobile applications using Flutter. I have also developed many desktop applications using Electronjs. My specialty is to develop any kind of web application. 
                            </p>
                            <v-btn tile dark class="yellow mt-4" variant="outlined">Download Resume</v-btn>
                        </v-col>
                    </v-row>
                </div>
            </v-col>
            <div class="text-center mt-4">
                <h2>What We Do</h2>
                <div style="width: 120px; text-align: center;">
                    <v-slider v-model="slider2" color="yellow" thumb-label="always"></v-slider>
                </div>
            </div>
            <v-col cols="12" class="padd" id="portfolio">
                <div class="first" id="project">
                    <v-row>
                        <v-col cols="12">
                            <div class="child">
                                <v-btn icon="fas fa-laptop" color="#FBDF7B" class="text-white"></v-btn>
                                <h3 class="ml-3 mt-4">Backend Developer</h3>
                                <p class="text-grey ml-3 mt-4 text-caption">
                                    Devops Engineer <br />
                                    Full Stack Developer <br />
                                    Fintech Solution Provider <br />
                                    Problem Solver <br />
                                </p>
                            </div>
                            <div class="child">
                                <v-btn icon="fas fa-mobile-alt" color="#FBDF7B" class="text-white"></v-btn>
                                <h3 class="ml-3 mt-4">Frontend Deveoper</h3>
                                <p class="text-grey ml-3 mt-4 text-caption">
                                    Devops Engineer <br />
                                    Full Stack Developer <br />
                                    Fintech Solution Provider <br />
                                    Problem Solver <br />
                                </p>
                            </div>
                            <div class="child">
                                <v-btn icon="fas fa-money-check-dollar" color="#FBDF7B" class="text-white"></v-btn>
                                <h3 class="ml-3 mt-4">Fintech Solution</h3>
                                <p class="text-grey ml-3 mt-4 text-caption">
                                    Devops Engineer <br />
                                    Full Stack Developer <br />
                                    Fintech Solution Provider <br />
                                    Problem Solver <br />
                                </p>
                            </div>
                        </v-col>
                    </v-row>
                    <v-divider></v-divider>
                </div>
            </v-col>
            <v-col cols="12" sm="12" id="services">
                <div class="d-flex justify-center mb-6">
                    <v-btn color="#FBDF7B" class="mr-2">All</v-btn>
                    <v-btn class="mr-2" variant="tonal">Backend Development</v-btn>
                    <v-btn class="mr-2" variant="tonal">Frontend Development</v-btn>
                    <v-btn class="mr-2" variant="tonal">Devops</v-btn>
                    <v-btn class="mr-2" variant="tonal">System Analysis</v-btn>
                    <v-btn class="mr-2" variant="tonal">Database Designer</v-btn>
                </div>
            </v-col>
            <v-col cols="12" class="imgHover">
                <v-row class="fill-height" align="center" justify="center">
                    <template v-for="(item, i) in items" :key="i">
                        <v-col cols="12" md="4">
                            <v-hover v-slot="{isHovering, props}">
                                <v-card :elevation="isHovering ? 12 : 2" :class="isHovering" v-bind="props">
                                    <v-img :src="item.img" cover height="225px"></v-img>
                                </v-card>
                            </v-hover>
                        </v-col>
                    </template>
                </v-row>
            </v-col>
            <v-col cols="12" sm="12">
                <div class="d-flex justify-center mb-6">
                    <v-btn color="#FBDF7B" class="mt-4">Load more</v-btn>
                </div>
            </v-col>
            <v-col cols="12" id="page">
                <div class="pre">
                    <v-row>
                        <v-col cols="12" sm="4" md="4">
                            <v-card class="mw-auto" max-width="300" height="">
                                <v-img src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" height="200px" cover></v-img>
                                <v-card-title>We Provide You the Best</v-card-title>
                                <v-card-subtitle>by zrshishir | 2023</v-card-subtitle>
                                <v-card-text>
                                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptate.
                                </v-card-text>
                            </v-card>
                        </v-col>
                        <v-col cols="12" sm="4" md="4">
                                <v-card class="mw-auto" max-width="300" height="">
                                    <v-img src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" height="200px" cover></v-img>
                                    <v-card-title>We Provide You the Best</v-card-title>
                                    <v-card-subtitle>by zrshishir | 2023</v-card-subtitle>
                                    <v-card-text>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptate.
                                    </v-card-text>
                                </v-card>
                            </v-col>
                            <v-col cols="12" sm="4" md="4">
                                <v-card class="mw-auto" max-width="300" height="">
                                    <v-img src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" height="200px" cover></v-img>
                                    <v-card-title>We Provide You the Best</v-card-title>
                                    <v-card-subtitle>by zrshishir | 2023</v-card-subtitle>
                                    <v-card-text>
                                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptate.
                                    </v-card-text>
                                </v-card>
                            </v-col>
                    </v-row>
                </div>
            </v-col>
            <v-col cols="12" id="blog">
                <div class="hire">
                    <v-row>
                        <v-col cols="12" sm="8">
                            <h1 class="mt-9">Hire Me for your awesome project</h1>
                            <p class="text-grey">
                                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptate.
                            </p>
                        </v-col>
                        <v-col cols="12" sm="4">
                            <v-btn color="#FBDF7B" class="mt-15">Hire Me</v-btn>
                        </v-col>
                    </v-row>
                </div>
            </v-col>
            <v-col cols="12" sm="12" class="px-16" id="contact">
                <v-row>
                    <v-col cols="12" sm="4">
                        <div class="child">
                            <h1>Contact Info</h1>
                            <v-btn icon="fas fa-marker-alt" class="mt-10" variant="outlined"></v-btn><br />
                            <span class="text-caption">Mirpur, Dhaka, Bangladesh</span><br />
                            <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br />
                            <span class="text-caption">017**********</span><br />
                            <span class="text-caption">017**********</span><br />
                            <v-btn icon="fas fa-envelop-alt" class="mt-10" variant="outlined"></v-btn><br />
                            <span class="text-caption">zrshishir@gmail.com</span><br />
                            <span class="text-caption">017**********</span><br />
                        </div>
                    </v-col>
                    <v-col cols="8" sm="8">
                        <h1 class="mt-8">Send your message</h1>
                        <v-divider></v-divider>
                        <span class="text-caption">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptate.</span>
                        <v-row class="mt-10">
                            <v-col cols="12" sm="6">
                                <v-text-field label="Name" persistent-hint variant="outlined"></v-text-field>
                            </v-col>
                            <v-col cols="12" sm="6">
                                <v-text-field label="Phone No" persistent-hint variant="outlined"></v-text-field>
                            </v-col>
                        </v-row>
                        <v-textarea label="Message" persistent-hint variant="outlined"></v-textarea>
                        <v-btn color="#FBDF7B" class="mt-4">Send Message</v-btn>
                    </v-col>
                </v-row>
            </v-col>
        </v-container>
        <FooterView />
    </v-app>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import FooterView from '../components/FooterView.vue';
export default {
    name: 'HomeView',
    setup() {
        return {
            slider2: 50,
            items: [
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                },
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                },
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                },
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                },
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                },
                {
                    img: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
                },
            ]
        }
    },
    components: {
        NavBar,
        FooterView
    },
    data: () => ({
        //
    }),
}
</script>

<style scoped>
    .v-container {
        padding: 16px 0;
    }
    .head {
        position: relative;
        text-align: center;
        padding: 12px;
        margin-bottom: 6px;
        height: 400px;
        width: 100%;
        color: white;
    }
    .head::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 50%;
        background: black;
        transform: skew(0deg, 6deg);
    }
    .head::after {
        content: '';
        position: absolute;
        top: 0;
        right: 0;
        height: 100%;
        width: 50%;
        background: black;
        transform: skew(0deg, -6deg);
    }
    .egg {
        display: block;
        margin-left: 100px;
        margin-top: 50px;
        width: 356px;
        height: 300px;
        background-color: #FBDF7E;
        border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
    }
    .first {
        width: 100%;
        height: 280px;
        text-align: center;
        padding: 2rem 2rem;
    }
    .child {
        display: inline-block;
        padding: 2rem 1rem;
        vertical-align: middle;
        text-align: center;
        margin-right: 8px;
    }
    .imgHover {
        padding: 0 200px;
    }
    .pre {
        width: 100%;
        height: 380px;
        text-align: center;
        padding: 0 200px;
        background-color: #f5f5f5;
    }
    .hire {
        width: 100%;
        height: 280px;
        text-align: center;
        padding: 0 200px;
        background-color: #e9e9e9;
        margin-top: -24px;
    }
</style>