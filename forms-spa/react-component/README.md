## AEM Form React Component for SPA - Editor
This package contains the AEM Form Component written in react to use in AEM SPA Editor.

## Steps:
The following steps document how to include an aemform component in AEM SPA Editor:
1) Download and unzip the latest [We.Retail journal code from Github](https://github.com/adobe/aem-sample-we-retail-journal).
2) Copy paste the AEM Form [react component](src/components/AEMForm.js) and [css](src/components/AEMForm.css) files, and the [test file](tests/AEMForm.test.js) to the [components](https://github.com/adobe/aem-sample-we-retail-journal/tree/master/react-app/src/components) and [tests](https://github.com/adobe/aem-sample-we-retail-journal/tree/master/react-app/tests) folder of react-app package in the downloaded source.
3) Include the aemform component in the [ImportComponent.js](https://github.com/adobe/aem-sample-we-retail-journal/blob/master/react-app/src/ImportComponents.js) file (add ```require('./components/AEMForm');```)
4) The aemform component uses jquery. Install jquery in the react-app node project using ```./node/npm install jquery --save```
5) Modify the [policy](https://github.com/adobe/aem-sample-we-retail-journal/blob/master/content/jcr_root/conf/we-retail-journal/react/settings/wcm/policies/.content.xml#L19) (content/jcr_root/conf/we-retail-journal/react/settings/wcm/policies/.content.xml) to include the aemform component resource type(fd/sample/af/components/aemform/v1/aemform)
6) Build and install the source package

## Limitations
1) Experience targeting and A/B tests configured in the original adaptive form do not work from the SPA app. 
2) If Adobe Analytics is configured on the original form, the analytics data is captured in Adobe Analytics server. However, it is not available in the Forms analytics report.

## SPA Editor
For getting started on developing and authoring Single Page Applications (SPAs) in AEM follow [here](https://helpx.adobe.com/experience-manager/6-4/sites/developing/user-guide.html?topic=/experience-manager/6-4/sites/developing/morehelp/spa.ug.js)
