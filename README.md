# Sugar Labs Highlight DDLB Field

Sugar Labs Highlight DDLB Field provides a new data type that provides the ability to assign colors to any DDLB field. Users can pick different colors for each DDLB entry in the list on a per field basis.

## Installation & Use
* Download the latest .tgz package here: https://github.com/sugarcrmlabs/HighlightDDLBField/releases/latest
* Load the package in your target instance using Module Loader
* Log in as an admin user
* Go to Studio and add a new field of type 'DDLB'
* You will see at the bottom of the new field screen each value of the DDLB list type selected
* Define what text color you want, and then what color you want each value to use


## Reports
* To implement report filtering, you will need to make core file changes:
    * sugar/modules/Reports/templates/templates_modules_def_js.php at line 495 by adding `filter_defs['HighLightfield'] = qualifiers;`.
    * sugar/include/javascript/reports.js at line 2957 by changing <br/>
    From: `} else if (field_type == 'enum' || field_type == 'multienum' || field_type == 'radioenum' || field_type == 'parent_type' || field_type == 'timeperiod' || field_type == 'currency_id') {` <br/>
    To: `} else if (field_type == 'enum' || field_type == 'multienum' || field_type == 'HighLightfield'  || field_type == 'radioenum' || field_type == 'parent_type' || field_type == 'timeperiod' || field_type == 'currency_id') {`

```
## Contributing
Everyone is welcome to contribute to this project! If you make a contribution, then the [Contributor Terms](CONTRIBUTOR_TERMS.pdf) apply to your submission.

Please check out our [Contribution Guidelines](CONTRIBUTING.md) for helpful hints and tips that will make it easier for us to accept your pull requests.

-----
Copyright (c) 2016 SugarCRM Inc. Licensed by SugarCRM under the Apache 2.0 license.
