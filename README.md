# cozy-style.scss
@charset "utf=8";
@use 'mixin' as mix;

// 変数
$main-color: #282926;
$w-color: #ffffff;
$main-font: 1.4vw;
$page-title-font: 4vw;
$sp-font: 12px;
$min-font: 10px;

//top.scss//

html {
    font-size: 100%;
}

img {
    max-width: 100%;
}

body {
    font-family: Righteous;
    font-family: 'Noto Sans JP', sans-serif;
}

.main-visual {
    background-color: $main-color;
    color: $w-color;
    display: flex;
    justify-content: center;
    padding-top: 4%;

    @include mix.mq(min) {
        align-items: flex-end;
    }

    &__wrap {
        position: relative;
        margin-right: 13%;
        padding-top: 4%;

        @include mix.mq(tab) {
            padding-top: 2%;
        }

        @include mix.mq(sp) {
            padding-top: 1%;
        }
    }

    &__img {
        width: 40vw;
    }

    &__title {
        font-family: 'Righteous';
        font-size: 2.5vw;
        padding-left: 10%;
    }

    &__subtitle {
        font-size: $main-font;
        padding-top: 8%;
        padding-left: 10%;

        @include mix.mq(tab) {
            font-size: 1.8vw;
        }

        @include mix.mq(sp) {
            display: none;
        }
    }

    &__text {
        font-size: $main-font;
        line-height: 4vw;
        padding-top: 10%;
        width: 36vw;
        padding-left: 10%;
        font-family: 'Noto Sans JP', sans-serif;

        @include mix.mq(tab) {
            font-size: 1.8vw;
        }

        @include mix.mq(sp) {
            font-size: $sp-font;
        }

        @include mix.mq(min) {
            font-size: $min-font;
        }
    }
}

.swiper--wrapper {
    /* wrapperのサイズを調整 */
    width: 6.5vw;
}

.swiper-slide {
    /* スライドのサイズを調整、中身のテキスト配置調整、背景色 */
    color: $w-color;
    width: 6.5vw;
    text-align: center;
}

.swiper-slide>img {
    width: 68%;

    @include mix.mq(sp) {
        width: 80%;
    }

    @include mix.mq(min) {
        width: 72%;
    }
}

.fadeUp {
    animation-name: fadeUpAnime;
    animation-duration: 1s;
    animation-fill-mode: forwards;
    opacity: 0;
}

@keyframes fadeUpAnime {
    from {
        opacity: 0;
        transform: translateY(100px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}


/* スクロールをしたら出現する要素にはじめに透過0を指定　*/

.fadeUpTrigger {
    opacity: 0;
}

.top__about {
    background-color: $main-color;
    color: $w-color;
    display: flex;
    justify-content: center;
    gap: 12vw;
    padding-top: 15%;
    padding-bottom: 10%;

    @include mix.mq(pc) {
        gap: 10vw;
    }

    &-img {
        width: 35vw;
        padding-top: 10vw;
    }

    &__text {
        font-size: $main-font;
        line-height: 5vw;
        padding-top: 8%;

        @include mix.mq(tab) {
            font-size: 1.8vw;
        }

        @include mix.mq(sp) {
            font-size: $sp-font;
            padding-top: 13%;
        }

        @include mix.mq(min) {
            font-size: $min-font;
        }
    }

    &-content {
        position: relative;
        width: 35vw;
    }

    &-btn {
        position: absolute;
        bottom: 10%;
        left: 60%;
    }
}


.btn {
    padding: 3% 8%;
    background-color: $w-color;
    color: $main-color;
    border-radius: 4px;
    font-size: $main-font;
}

.button {
    position: relative;
    display: block;
    padding: 2% 4%;
    background-color: $main-color;
    border: 1px solid $w-color;
    color: $w-color;
    text-align: center;
    text-decoration: none;
    margin-left: 21vw;
    margin-top: 4vw;
    font-size: $main-font;

    @include mix.mq(tab) {
        margin-left: 18vw;

    }

    @include mix.mq(sp) {
        margin-left: 15vw;
    }

    @include mix.mq(min) {
        margin-top: 0;
    }

    &:hover {
        box-shadow: 0 5px 10px #F6F4EF;
        transform: translate(0, -5px);
    }
}

.button_1 {
    position: absolute;
    top: 69%;
    right: 5%;
    font-size: $main-font;
    margin-left: 10vw;
    

    @include mix.mq(tab) {
        padding: 4% 3%;
        top: 66%;
    }


    @include mix.mq(ro) {
        padding: 3% 2%;
        right: 2%;
        top: 71%;
    }

    @include mix.mq(sp) {
        font-size: $sp-font;
        padding: 3% 2%;
        top: 77%;
        right: 1%;
    }

    @include mix.mq(min) {
        font-size: $min-font;
        top: 84%;
        padding: 2%;
    }
    &:hover {
        box-shadow: 0 5px 10px #282926;
        transform: translate(0, -5px);
    }

}

.button_2 {
    top: 68%;

    @include mix.mq(tab) {
        top: 69%;

    }

    @include mix.mq(sp) {
        top: 72%;
    }

    @include mix.mq(min) {
        top: 82%;
    }
}

.button:hover::after {
    animation: arrow .5s;
}

@keyframes arrow {
    100% {
        transform: rotateX(360deg);
    }
}

.fade-in {
    font-size: 40px;
    opacity: 0;
    animation-name: About;
    animation-duration: 7s;
    animation-fill-mode: forwards;
}

@keyframes About {
    0% {
        opacity: 0;
        transform: translateX(-50px);
    }

    50% {
        opacity: 5;
        transform: translateX(0);
    }

    100% {
        opacity: 1;
    }
}

.page-header {
    position: relative;
    font-size: $page-title-font;
    margin-left: 1vw;
    font-family: 'Righteous';

    &::before {
        content: "";
        position: absolute;
        height: 2px;
        width: 15vw;
        bottom: 40%;
        right: 102%;
        background: orange;
    }
}

.menu {
    background-image: url(../img/haikei.webp);
    background-size: cover;
    padding: 0% 3% 5%;

    @include mix.mq(sp) {
        padding-bottom: 8%;
    }

    &__page-header1 {
        text-align: center;
        font-size: $page-title-font;
        font-weight: bold;
        font-family: 'Righteous';
        padding-top: 5%;
    }

    &__text {
        text-align: center;
        font-size: 1.8vw;
        padding-bottom: 2%;
        padding-top: 2%;

        @include mix.mq(sp) {
            font-size: $sp-font;
        }

        @include mix.mq(min) {
            font-size: $min-font;
        }
    }

    &__item {
        display: flex;
        justify-content: center;
    }

    &__top-title {
        padding: 0% 12%;
    }

    &__title {
        font-size: 2.5vw;
        align-items: center;
        padding-top: 5%;

        @include mix.mq(tab) {
            padding: 5% 0;
        }

        @include mix.mq(sp) {
            font-size: 16px;
        }

        & span {
            color: orange;
            font-size: $page-title-font;
        }
    }

    &__sub-title {
        font-size: $main-font;
        line-height: 0.5vw;
        margin-left: 5vw;
        margin-bottom: 5%;

        @include mix.mq(tab) {
            display: none;
        }
    }

    &__contents {
        width: 33%;
    }

    &__contents1 {
        width: 45%;
        background-color: $w-color;
        padding: 3%;
        position: relative;

        &-text {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
    }

    &-img &-img1 {
        width: 50%;
    }


    &__title1 {
        font-size: 2.2vw;

        @include mix.mq(sp) {
            font-size: $sp-font;
        }

    }

    &__info {
        font-size: $main-font;

        @include mix.mq(sp) {
            padding-right: 5%;
            font-size: $min-font;
        }


    }

    &__sub-title1 {
        font-size: $main-font;
        margin-top: 3%;

        @include mix.mq(tab) {
            display: none;
        }
    }

    &__text1 {
        font-size: $main-font;
        margin-top: 5%;
        text-align: initial;

        @include mix.mq(sp) {
            font-size: $sp-font;
        }

        @include mix.mq(min) {
            font-size: $min-font;
        }
    }

    &__img1 {
        margin-top: 8%;
        width: 60%;
    }

    &-btn {
        position: absolute;
        background-color: $main-color;
        color: $w-color;
        padding: 2% 4%;
        right: 5vw;
        bottom: 20%;
    }
}

// news
.news {
    &__ly {
        background-color: #F6F4EF;
        padding-left: 13vw;
        padding-right: 13vw;
        padding-top: 5%;
        position: relative;
    }

    &-page-header {
        font-family: 'Righteous';
        font-size: $page-title-font;
        text-align: center;
        padding-top: 5%;
    }

    &__info {
        padding: 5% 14%;

        @include mix.mq(min) {
            padding: 5% 3%;
        }
    }

    &__content {
        padding: 4% 3%;
        background: $w-color;
        border-top: 1px solid black;
        border-left: 1px solid black;
        border-right: 1px solid black;
        list-style: none;
        font-size: $main-font;
        display: flex;

        @include mix.mq(sp) {
            font-size: 11px;
        }

        @include mix.mq(min) {
            font-size: $min-font;
        }

        &:last-child {
            border-bottom: 1px solid black;
        }

        & span {
            width: 65vw;
            margin-left: 3vw;

            @include mix.mq(min) {
                width: 71vw;

            }
        }
    }
}

//about.scss//
$min-font: 10px;


.about {
    &__bg {
        background-color: #F6F4EF;
        position: relative;
        padding-bottom: 10%;

        @include mix.mq(tab) {
            padding-bottom: 5%;
        }
    }
    &__text{
        @include mix.mq(tab) {
            font-size: 14px;
        }
        @include mix.mq(sp) {
            font-size: 11px;
        }
        @include mix.mq(min) {
            font-size: $min-font;
        }
    }
    &__page-header {
        font-size: 4rem;
        font-family: 'Righteous';
        margin-left: 44%;
        padding-top: 6%;
        padding-bottom: 3%;

        @include mix.mq(pc) {
            font-size: 6vw;
            margin-left: 39%;
        }

        &::before {
            content: "";
            position: absolute;
            height: 2px;
            width: 50vw;
            top: 57%;
            right: 56%;
            background: orange;

            @include mix.mq(pc) {
                right: 61%;
            }
        }
    }

    &__page-title {
        font-size: 1.8rem;
        padding-left: 13%;
        font-family: 'Righteous';

        @include mix.mq(tab) {
            font-size: 3.6vw;
            padding-left: 11%;
        }
    }

    &__content {
        display: flex;
        justify-content: space-around;
        width: 100%;
        padding: 3% 0 9%;
        @include mix.mq(sp) {
            display: flex;
            justify-content: flex-start;
        }

    }

    &__sub-title {
        font-weight: bolder;
        font-family: 'Righteous';
        font-size: 3vw;
        padding: -0.5em 0;
        @include mix.mq(sp) {
            padding-bottom: 2%;
        }
    }

    &__img {
        width: 50%;
        text-align: center;
    }

    &__img1 {
        width: 60%;
    
    }

    &__concept {
        width: 44%;
        font-size: 1.8vw;
        font-weight: lighter;
        white-space: nowrap;
        
        
        @include mix.mq(sp) {
            width: 40%;
            white-space: inherit;
        }

        

        & br{
            display: block;
            @include mix.mq(sp) {
                display: none;
            }
        }
    }

    &__main-visual {
        margin: 0 auto 0;
        padding: 4% 0 10% 0;
        background-color: #282926;
    }

    &__box {
        width: 65vw;
        background-color: #fff;
        margin:10% auto 5%;
        border-radius: 30px;
        padding: 4% 0;
        box-shadow: 0 10px 25px 0 rgba(0, 0, 0, .5);

        @include mix.mq(tab) {
            margin: 12% auto 10%;
        }
    }

    &__message-title {
        text-align: center;
        font-family: 'Righteous';
        font-weight: bold;
        font-size: 4vw;

        @include mix.mq(tab) {
            padding-bottom: 5%;
        }

        @include mix.mq(sp) {
            font-size: 1.5rem;

        }
    }

    &__message-text {
        padding: 15px 20%;
        line-height: 3.5rem;
        text-align: initial;

        @include mix.mq(pc) {
            padding: 0px 14%;
        }

        @include mix.mq(tab) {
            padding: 0px 8%;
            line-height: 2.5rem;
            font-size: 2vw;
        }

        @include mix.mq(sp) {
            line-height: 1.5rem;
            font-size: 11px;
        }
        @include mix.mq(min) {
            font-size: $min-font;
        }
    }

}


.slider {
    display: flex;
    justify-content: space-around;
    margin: 0 10px;

    & img {
        object-fit: cover;
        margin-top: 15%;
    }

    &-slide {
        margin: 0 10px;
        
    }
}

//menu.scss//
.menu {
    &__inner {
        padding: 0 30px;
        padding-bottom: 5%;
        width: 50%;
    }

    &__img-w {
        width: 100%;
        height: auto;
    }

    &__bg {
        background-color: #F6F4EF;
        background-size: cover;
    }

    &__page-header {
        position: relative;
        font-size: 4rem;
        margin-left: 45vw;
        font-family: 'Righteous';
        padding-top: 6%;
        padding-bottom: 5%;

        @include mix.mq(pc) {
            font-size: 6vw;
        }

        &::before {
            content: "";
            position: absolute;
            height: 2px;
            width: 50vw;
            bottom: 42%;
            right: 100%;
            background: orange;
        }
    }

    &__ly {
        width: 100%;
        margin: 0 auto;
        box-sizing: border-box;
    }

    &__cafe-coffee-title {
        background: url(../img/menu-coffee.png) no-repeat;
        padding-top: 30%;
        background-size: cover;
        background-position: center;
        position: relative;
        font-weight: 300;

        & h3 {
            position: absolute;
            top: 50%;

            left: 50%;
            letter-spacing: 4px;
            font-size: $main-font;
            transform: translateY(-50%) translateX(-50%);
            font-family: "Righteous";
            color: #F6F4EF;

        }
    }

    &__cafe h4 {

        font-weight: 300;
        font-family: "Oswald", sans-serif;
        text-align: center;
        margin: 5%;
        letter-spacing: 4px;

        & span {
            border-bottom: 1px solid #231815;
            font-size: 2rem;
            padding: 0;

            @include mix.mq(ro) {
                font-size: $sub-font;
            }
        }
    }

    &__cafe-list {
        display: flex;
        -webkit-flex-wrap: wrap;
        flex-wrap: wrap;

        & p {
            font-size: 1.4vw;
            font-weight: 300;

            @include mix.mq(tab) {
                font-size: 1.8vw;
                bottom: -80px;
            }
        }
    }

    &__cafe_pasta_title {
        background: url(../img/menu-pasta.png);
        padding-top: 30%;
        background-size: cover;
        background-position: center;
        position: relative;
        font-weight: 300;

        & h3 {
            position: absolute;
            top: 50%;

            left: 50%;
            letter-spacing: 4px;
            font-size: $main-font;
            transform: translateY(-50%) translateX(-50%);
            font-family: "Righteous";
            color: #F6F4EF;
        }
    }


    &__cafe_dessert_title {
        background: url(../img/menu-dessert.png) no-repeat;
        padding-top: 30%;
        background-size: cover;
        background-position: center;
        position: relative;
        font-weight: 300;

        & h3 {
            position: absolute;
            top: 50%;

            left: 50%;
            letter-spacing: 4px;
            font-size: $main-font;
            transform: translateY(-50%) translateX(-50%);
            font-family: "Righteous";
            color: #F6F4EF;
        }
    }

    &__price {
        font-size: $sub-font;
        padding: 3% 0;
        font-weight: 300;

        @include mix.mq(tab) {
            width: 43%;
        }

        @include mix.mq(ro) {
            font-size: 1rem;
        }
    }

    &__normal {
        width: 100%;
        position: relative;
        padding: 5% 0;
        font-size: 16px;

        @include mix.mq(sp) {
            font-size: $min-font;
        }
    }
}

h5 {
    font-size: $sub-font;
    padding-bottom: 3%;

    @include mix.mq(ro) {
        font-size: 0.8rem;
    }
}

tbody {
    display: table-row-group;
    vertical-align: middle;
    border-color: inherit;
    text-align: left;
    font-weight: 300;
}

td {
    font-size: 20px;
    text-align: right;
    padding: 2% 0;
    color: #000;
    vertical-align: bottom;
    white-space: nowrap;
    font-weight: 300;

    @include mix.mq(ro) {
        font-size: 13px;
    }

    @include mix.mq(sp) {
        font-size: $sp-font;
    }

    @include mix.mq(min) {
        font-size: $min-font;
    }
}

th {
    font-size: 20px;
    font-weight: 300;
    padding: 2% 0;
    color: #000;

    @include mix.mq(ro) {
        font-size: 13px;
    }

    @include mix.mq(sp) {
        font-size: $sp-font;
    }

    @include mix.mq(min) {
        font-size: $min-font;
    }
}
//access.scss//
.access {
    &__bg {
        background-color: #F6F4EF;
        position: relative;
        padding-bottom: 10%;
        @include mix.mq(pc) {
            padding-bottom: 5%;
        }
    }

    &__page-header {
        font-size: 4rem;
        font-family: 'Righteous';
        margin-left: 41%;
        padding-top: 7%;
        padding-bottom: 3%;

        @include mix.mq(pc) {
            font-size: 6vw;
        }

        &::before {
            content: "";
            position: absolute;
            height: 2px;
            width: 50vw;
            top: 60%;
            right: 60%;
            background: orange;
        }
    }
   

    &__flex {
        display: flex;
        justify-content: space-between;

        @include mix.mq(pc) {
            display: block;
        }

    }

    &__map {
        width: 70%;

        @include mix.mq(pc) {
            width: 100%;
        }
       
    }
    &__map1{
        @include mix.mq(sp) {
            height: 200px;
        }
    }

    &__info {
        width: 25%;

        @include mix.mq(pc) {
            width: 100%;
            display: flex;
            justify-content: space-between;
            padding: 5% 13%;
        }

        @include mix.mq(tab) {
            padding: 5% 6%;
        }

        & ul {
            list-style-type: none;
        }

        &-item {
            width: 100%;
            line-height: 2;

            @include mix.mq(pc) {
                background-color: #fff;
                padding: 2%;
            }

            @include mix.mq(tab) {
                width: 42%;
            }

            @include mix.mq(sp) {
                width: 48%;
            }

        }

        &-subitem {
            width: 100%;
            line-height: 2;

            @include mix.mq(pc) {
                margin-left: 20%;
                background-color: #fff;
                padding: 2%;
            }

            @include mix.mq(tab) {
                margin-left: 10%;
                width: 42%;
            }

            @include mix.mq(sp) {
                width: 48%;
            }
        }
    }

    &__title {
        font-size: 1.5rem;
        @include mix.mq(tab) {
            font-size: 1rem;
        }
    }

    &__text {
        text-align: left;
        white-space: nowrap;

        @include mix.mq(tab) {
            font-size: 2vw;
        }

        & span {
            font-size: 2vw;
            padding-left: 1vw;
        }
    }
}

iframe {
    width: 100%;
}


/*contact*/
.contact {
    position: relative;

    &__page-header {
        font-size: 4rem;
        font-family: 'Righteous';
        margin-left: 41%;
        padding-top: 7%;
        padding-bottom: 3%;

        @include mix.mq(pc) {
            font-size: 6vw;
        }
        @include mix.mq(tab) {
           margin-left: 39%;
        }

        &::before {
            content: "";
            position: absolute;
            height: 2px;
            width: 45vw;
            top: 60%;
            right: 60%;
            background: orange;
            @include mix.mq(tab) {
                right: 62%;
            }
        }
    }
    &__img{
        width: 10%;
    }

    &__text {
        text-align: center;
        font-size: 1.8vw;
        font-weight: normal;

        @include mix.mq(pc) {
            font-size: 1.6vw;
        }
        @include mix.mq(sp) {
            font-size: 12px;
        }

        @include mix.mq(min) {
            font-size: 10px;
        }
    }

    &__box {
        box-sizing: border-box;
        border: 2px solid #282926;
        margin: 10% auto;
        text-align: center;
        width: 75%;

        @include mix.mq(pc) {
            margin: 7% auto;
        }
    }

    &__info {
        display: flex;
        align-items: center;
        gap: 2vw;
        padding: 4% 0 4% 24vw;

        @include mix.mq(pc) {
            padding: 4% 0 4% 27vw;
        }
        @include mix.mq(tab) {
            padding: 4% 0 4% 26vw;
        }
       
    }

    &__number,
    &__addres {
        font-size: 2vw;
    }
}
