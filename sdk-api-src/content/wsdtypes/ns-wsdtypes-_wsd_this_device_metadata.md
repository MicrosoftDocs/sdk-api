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

# _WSD_THIS_DEVICE_METADATA structure


## -description


Specifies metadata that is unique to a specific device.


## -struct-fields




### -field FriendlyName

Reference to a <a href="https://msdn.microsoft.com/4941885c-d349-4e43-838f-b60c3cdc32ba">WSD_LOCALIZED_STRING_LIST</a> structure that contains the list of localized friendly names for the device. It should be set to fewer than 256 characters.


### -field FirmwareVersion

The firmware version of the device. It should be set to fewer than 256 characters.


### -field SerialNumber

The serial number of the device. It should be set to fewer than 256 characters.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that provides an extensible space for devices to add custom metadata to the device specific section. For example, you can use this to add a user-defined name for the device. 


## -remarks



ThisDevice metadata follows this form:



<pre class="syntax" xml:space="preserve"><code>&lt;wsd:ThisDevice&gt;
    &lt;wsd:FriendlyName&gt;
        A. Datum WebWeigh Scale
    &lt;/wsd:FriendlyName&gt;
    &lt;wsd:FirmwareVersion&gt;
        2.53c
    &lt;/wsd:FirmwareVersion&gt;
    &lt;wsd:SerialNumber&gt;
        923450982349058
    &lt;/wsd:SerialNumber&gt;
 &lt;/wsd:ThisDevice&gt;</code></pre>


