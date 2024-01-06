<template>

    <div class="mainveil" v-if="is_expanded"></div>

  <div class="headercontainer">
    <div class="header">
        <div class="logo">
            <img src="../assets/whitelogo2.png" alt="proselogo">
            <h1>LawBy<span>You</span></h1>
            <h2>Pro-Se Legal Help</h2>
        </div>
        <div class="hamburger" :class="{ 'is-active': is_expanded }" @click="ToggleMenu">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>
        
    </div>
    <div class="menuslidelist" :class="{ 'is-expanded': is_expanded }">


            <div class="home" ><a href="">Home</a></div>
            <div class="about" :class="{ 'isaboutexpanded': isaboutexpanded }" @click="toggleabout">
                <div class="textandsvg">
                    <p>About LawByYou</p>
                    <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='30' height='30'><path d="M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z"></path></svg>
                </div>
                <div class="aboutcontent" >
                <li>
                    <a href="">Who We Are </a>

                </li>
                <li>
                    <a href="">What We Do</a>

                </li>
                <li>
                    <a href="">Our Team And Partners </a>
                </li>
                </div>
            </div>
            <div class="prose" :class="{ 'isproseexpanded': isproseexpanded }" @click="toggleprose">                
                <div class="textandsvg">
                    <p>Prose</p>
                    <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='30' height='30'><path d="M16.293 9.293 12 13.586 7.707 9.293l-1.414 1.414L12 16.414l5.707-5.707z"></path></svg>
                </div>

            <div class="prosecontent">
                <li>
                <a href="">Family Law</a>
                    </li>
                <li>
                    <a href="">Pro Se (Self Representation)</a>
                </li>
                <li>
                    <a href="">Pro Se Law Resources</a>
                </li>
                <li>
                    <a href="">Case Filling</a>
                </li>
                <li>
                    <a href="">Appearing Without an Attorney</a>
                </li>
                <li>
                    <a href="">Services for Pro Se</a>
                </li>
                <li>
                    <a href="">Forms (Pro Se)</a>
                </li>
                <li>
                    <a href="">Legal Assistance Clinic</a>
                </li>

            </div>
            </div>
           
            <div class="successstories"><a href="">Success Stories</a></div>
            <div class="blog"><a href="">Blog</a></div>
            <div class="faq"><a href="">Faq</a></div>
            <div class="contactus"><a href="">Contact US</a></div>



    </div>
    </div>

    <div class="herosection">
        <img src="../assets/lawbackground3.jpg" alt="">
        <div class="veil"></div>
        <div class="texts">
            <h1 ref="title" class="title">"Everything you need <br>to effectively represent <br> yourself in court"</h1>
            <button ref="button" class="button">Schedule a Consult</button>
        </div>
    </div>
    <div class="sections" :class="{ 'is-expanded': is_expanded }">
        <div class="section1">
            <h1 ref="header" class="header">
                Prose Legal

            </h1>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>
            <p ref="para1" class="para1">
                Lorem, ipsum dolor sit amet consectetur
                 adipisicing elit. Dignissimos, ullam impedit quae adipisci sapiente esse fugit nulla? Libero tenetur doloribus, dolorum assumenda quia 
                 adipisci dicta, illum nulla soluta incidunt sunt.
            </p>

        </div>
        <div class="section2">
            <div ref="fam">
                 <h3>Family Law</h3>
            </div >
            <div ref="crim">
                 <h3>Criminal Law</h3>
            </div >
            <div ref="imm">
                 <h3>Immigration Law</h3>
            </div>
            <div ref="forms">
                 <h3>Forms</h3>
            </div>
            <div ref="etc">
                 <h3>ETC</h3>
            </div>
            <div ref="etcc">
                 <h3>ETC</h3>
            </div>
        
        </div>
    </div>
    <div class="footer" >
                <div class="logo">
            <img src="../assets/whitelogo2.png" alt="proselogo">
            <p>Updates coming soon </p>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const is_expanded = ref(false)

const ToggleMenu = () => {
    is_expanded.value = !is_expanded.value;
}
const isaboutexpanded = ref(true)

const toggleabout = () => {
    // isaboutexpanded.value = !isaboutexpanded.value;
}

const isproseexpanded = ref(true)

const toggleprose = () => {
    // isproseexpanded.value = !isproseexpanded.value;
}



import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
gsap.registerPlugin(ScrollTrigger);

  const title = ref(null);
  const button = ref(null);

onMounted(() => {

  gsap.from(title.value, {
        delay:1,
    opacity: 0,
    duration: 1.5,
    ease: 'back.out(1.7)',

  });

  gsap.from(button.value, {
    delay:1,
    opacity: 0,
    y: 17,
    duration: 0.9,
    ease: 'power2.out',

  });

});

const fam = ref(null);
const crim = ref(null);
const imm = ref(null);
const forms = ref(null);
const etc = ref(null);
const etcc = ref(null);

onMounted(() => {
  // Consolidated GSAP Timeline
  const masterTimeline = gsap.timeline();

  // Define animations within the master timeline
  masterTimeline
    .from(fam.value, { x: '60', opacity: 0, duration: 1, ease: 'power.in' }, '-=0.5')
    .from(crim.value, { x: '-60', opacity: 0, duration: 1, ease: 'power.in' }, '-=0.5') // Delayed by 0.5s
    .from(imm.value, { x: '60', opacity: 0, duration: 1, ease: 'power.in' }, '-=0.8') // Delayed by 1s
    .from(forms.value, { x: '-60', opacity: 0, duration: 1, ease: 'power.in' }, '-=1.5') // Delayed by 1s
    .from(etc.value, { x: '60', opacity: 0, duration: 1, ease: 'power.in' }, '-=1.8') // Delayed by 1s
    .from(etcc.value, { x: '-60', opacity: 0, duration: 1, ease: 'power.in' }, '-=1.7'); // Delayed by 1s

  // Use a single ScrollTrigger for all animations
  ScrollTrigger.create({
    trigger: fam.value, // You can use any of your elements as a trigger
    start: 'top 90%',
    end: '500% 90%',
    animation: masterTimeline,
    // scrub: true,
    // markers: true,
  });
});

</script>

<style lang="scss">
@import '../sass/main.scss';
 </style>