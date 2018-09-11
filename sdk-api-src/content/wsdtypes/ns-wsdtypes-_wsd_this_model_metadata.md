---
UID: NS:wsdtypes._WSD_THIS_MODEL_METADATA
title: "_WSD_THIS_MODEL_METADATA"
author: windows-sdk-content
description: Provides model-specific information relating to the device.
old-location: ncd\wsd_this_model_metadata_struct.htm
tech.root: WsdApi
ms.assetid: 614daaeb-76ac-4dec-93fe-f413164d5330
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSD_THIS_MODEL_METADATA, WSD_THIS_MODEL_METADATA structure, _WSD_THIS_MODEL_METADATA, ncd.wsd_this_model_metadata_struct, wsdtypes/WSD_THIS_MODEL_METADATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_THIS_MODEL_METADATA
product: Windows
targetos: Windows
req.typenames: WSD_THIS_MODEL_METADATA
req.redist: 
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


