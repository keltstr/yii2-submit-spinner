Yii2 Submit Spinner
===================


**December 12, 2014**


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

`
php composer.phar require --prefer-dist "c006/yii2-submit-spinner" "dev-master"
`

or add

`
"c006/yii2-submit-spinner": "dev-master"
`

to the require section of your `composer.json` file.


Required
--------

+ ***jQuery***

+ **yii \ widgets \ ActiveForm**

>
    <?php $form = ActiveForm::begin([
            'id' => 'form-id',
            'options' => [ 'class' => 'form-login', 'role' => 'form' ],
            // 'beforeSubmit' => 'c006_show_spinner', /* No longer used */
        ]
    );
    ?>

**Remove** this line from previous installs
`'beforeSubmit' => 'c006_show_spinner',`



Options
-------

**form_id =>**  {string}  
` The ID of the form `

**bg_color =>**  {string}  
` Color of the overlay `

**bg_opacity =>**  {float}  
` Opacity of the overlay `

**spin_speed =>**  {int}  
` How many seconds a for a complete 360 rotation `

**radius =>**  {int}  
` Pixel radius/width of the spinner `

**bg_spinner_opacity =>**  {float}  
` Opacity of  main spinner`

**bg_spinner_color =>**  {string}  
` Color of  main spinner `

**sections =>**  {int}  
` How many dots or circles `

**section_size =>**  {int}  
` Dot/circle size in px `

**section_color =>**  {string}  
` Color of dots/circles `

**section_offset =>**  {int}  
` How far from the center in px `

**section_opacity_base =>**  {float}  
` Minimum opacity e.g. 0.25 `

**proportionate_increase =>**  {boolean}  
` Will increase/decrease dots proportionally to the main spinner `





Usage
-----

Demo: [http://demo.c006.us/index.php?r=demo/submit-spinner](http://demo.c006.us/index.php?r=demo/submit-spinner)

Once the extension is installed, simply use it in your code by  :




**Defaults option:**

>
    <?= \c006\spinner\SubmitSpinner::widget(); ?>



**All options:**
_(using defaults)_

>
    <?=
        c006\spinner\SubmitSpinner::widget(
                               [
                                   'form_id'                => $form->id,
                                   'bg_color'               => '#444444',
                                   'bg_opacity'             => 0.8,
                                   'spin_speed'             => 4,
                                   'radius'                 => 200,
                                   'bg_spinner_opacity'     => 0.5,
                                   'bg_spinner_color'       => '#000000',
                                   'sections'               => 15,
                                   'section_size'           => 20,
                                   'section_color'          => '#FFFFFF',
                                   'section_offset'         => 80,
                                   'section_opacity_base'   => .2,
                                   'proportionate_increase' => 1,
                               ]
        ) ?>


**All options:**
_(5 large dots only, no background spinner)_


>
    <?= c006\spinner\SubmitSpinner::widget(
                                  [
                                      'form_id'                => $form->id,
                                      'bg_color'               => '#333333',
                                      'bg_opacity'             => 0.8,
                                      'spin_speed'             => 4,
                                      'radius'                 => 250,
                                      'bg_spinner_opacity'     => 0.0,
                                      'bg_spinner_color'       => '#000000',
                                      'sections'               => 5,
                                      'section_size'           => 80,
                                      'section_color'          => '#FFFFFF',
                                      'section_offset'         => 80,
                                      'section_opacity_base'   => .2,
                                      'proportionate_increase' => 0,
                                  ]
           ) ?>


Errors
---------

If you see this error.

![Error Message](http://github.c006.us/yii2-submit-spinner/alert.jpg)

In this file `vendor/c006/yii2-submit-spinner/assets/AppAssets.php`

comment out these lines.

>
        public $depends = [
            // 'yii\web\YiiAsset',
            // 'yii\widgets\ActiveFormAsset',
            // 'yii\bootstrap\BootstrapAsset',
        ];


Comments / Suggestions
--------------------

Please provide any helpful feedback or requests.

Thanks.


































