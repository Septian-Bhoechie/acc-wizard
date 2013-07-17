# acc-wizard

An accordion-based wizard based on Bootstrap styles.

This wizard is implemented as a jQuery plugin. Include the appropriate CSS and javascript files in your HTML, and then activate the wizard by calling it, e.g.

    $(window).load(function() {
                $(".acc-wizard").accwizard();
    })

For a demonstration and example usage, see [here](http://sathomas.me/acc-wizard/).

## Options

The plugin accepts options as a single object argument. Supported options are:

* **addButtons** add next/prev buttons to panels (default: true)
* **sidebar** selector for task sidebar (default: ".acc-wizard-sidebar")
* **activeClass** class to indicate the active task in sidebar (default: "acc-wizard-active")
* **completedClass** class to indicate task is complete (default: "acc-wizard-completed")
* **todoClass** class to indicate task is still pending (default: "acc-wizard-todo")
* **stepClass** class for step buttons within panels (default: "acc-wizard-step")
* **nextText** text for next button (default: "Next Step")
* **backText** text for back button (default: "Go Back")
* **nextType** HTML input type for next button (default: "submit")
* **backType** HTML input type for back button (default: "reset")
* **nextClasses** class(es) for next button (default: "btn btn-primary")
* **backClasses** class(es) for back button (default: "btn")
* **beforeNext** function to call before going to next step, return true to proceed to the next step; others to stop. e.g. used for validation
* **onNext** function to call on next step
* **beforeBack** function to call before going to previous step, return true to proceed to the next step; others to stop
* **onBack** function to call on back up
* **onInit** a chance to hook initialization
* **onDestroy** a chance to hook destruction

## Public Methods

Public methods could be retrieved:
    
    $('#last-step-back-button').click $(".acc-wizard").accwizard('go_prev')

or called by supplying arguments:

    $(".acc-wizard").accwizard('show_step', 1)

Public methods list:

* **option** Get/set a plugin option: $('#el').accwizard('option', 'addButtons') and $('#el').accwizard('option', 'addButtons', true)
* **destroy** Destroy plugin: $('#el').accwizard('destroy')()
* **go_next** Go to next step
* **go_prev** Go back to previous step
* **show_step** Go to accordion step, starting from 1
