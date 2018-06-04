---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WSD_THIS_MODEL_METADATA structure


## -description


Provides model-specific information relating to the device.


## -struct-fields




### -field Manufacturer

Reference to a <a href="https://msdn.microsoft.com/4941885c-d349-4e43-838f-b60c3cdc32ba">WSD_LOCALIZED_STRING_LIST</a> structure that contains the manufacturer name. The name should be set to fewer than 2048 characters.


### -field ManufacturerUrl

The URL to a Web site for the device manufacturer. The URL should have fewer than 2048 characters.


### -field ModelName

Reference to a <a href="https://msdn.microsoft.com/4941885c-d349-4e43-838f-b60c3cdc32ba">WSD_LOCALIZED_STRING_LIST</a> structure that specifies model names. This is a list of localized friendly names that should be set to fewer than 256 characters.


### -field ModelNumber

The model number. This should be set to fewer than 256 characters.


### -field ModelUrl

The URL to a Web site for this device model. The URL should have fewer than 2048 characters.


### -field PresentationUrl

An HTML page for this device. This can be relative to a base URL set by XML Base. The URL should have fewer than 2048 characters.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.


## -remarks



<b>WSD_THIS_MODEL_METADATA</b> specifies manufacturer metadata that is common to all instances of a specific model.





Model metadata follows this form:

<pre class="syntax" xml:space="preserve"><code>&lt;wsd:ThisModel&gt;
    &lt;wsd:Manufacturer&gt;
        A. Datum Corporation
    &lt;/wsd:Manufacturer&gt;
    &lt;wsd:ManufacturerURL&gt;
        http://www.adatum.com
    &lt;/wsd:ManufacturerURL&gt;
    &lt;wsd:ModelName&gt;
        WebWeigh
    &lt;/wsd:ModelName&gt;
    &lt;wsd:ModelNumber&gt;
        9-23492-83049
    &lt;/wsd:ModelNumber&gt;
    &lt;wsd:ModelURL&gt;
        http://www.adatum.com/WebWeighOwner.html 
    &lt;/wsd:ModelURL&gt;
    &lt;wsd:PresentationURL&gt;
        presentation/menu.html
    &lt;/wsd:PresentationURL&gt;
&lt;/wsd:ThisModel&gt;


</code></pre>


