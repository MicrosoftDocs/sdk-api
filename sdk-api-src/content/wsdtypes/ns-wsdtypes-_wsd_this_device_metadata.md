---
UID: NS:wsdtypes._WSD_THIS_DEVICE_METADATA
title: "_WSD_THIS_DEVICE_METADATA"
author: windows-sdk-content
description: Specifies metadata that is unique to a specific device.
old-location: ncd\wsd_this_device_metadata_struct.htm
old-project: WsdApi
ms.assetid: 7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSD_THIS_DEVICE_METADATA, WSD_THIS_DEVICE_METADATA structure, _WSD_THIS_DEVICE_METADATA, ncd.wsd_this_device_metadata_struct, wsdtypes/WSD_THIS_DEVICE_METADATA
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
req.idl: Wsdhost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_THIS_DEVICE_METADATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_THIS_DEVICE_METADATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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


