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

# _STORAGE_PROPERTY_QUERY structure


## -description


Indicates the properties of a storage device or adapter to retrieve as the input buffer passed to the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code.


## -struct-fields




### -field PropertyId

Indicates whether the caller is requesting a device descriptor, an adapter descriptor, a write cache 
      property, a device unique ID (DUID), or the device identifiers provided in the device's SCSI vital product data 
      (VPD) page. For a list of the property IDs that can be assigned to this member, see 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff566996">STORAGE_PROPERTY_ID</a>.


### -field QueryType

Contains flags indicating the type of query to be performed as enumerated by the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff566998">STORAGE_QUERY_TYPE</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PropertyStandardQuery"></a><a id="propertystandardquery"></a><a id="PROPERTYSTANDARDQUERY"></a><dl>
<dt><b>PropertyStandardQuery</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Instructs the port driver to report a device descriptor, an adapter descriptor or a unique hardware 
        device ID (DUID).

</td>
</tr>
<tr>
<td width="40%"><a id="PropertyExistsQuery"></a><a id="propertyexistsquery"></a><a id="PROPERTYEXISTSQUERY"></a><dl>
<dt><b>PropertyExistsQuery</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Instructs the port driver to report whether the descriptor is supported.

</td>
</tr>
</table>
 


### -field AdditionalParameters

Contains an array of bytes that can be used to retrieve additional parameters for specific queries.


## -remarks



The optional output buffer returned through the <i>lpOutBuffer</i> parameter of the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> control code can 
     be one of several structures depending on the value of the <b>PropertyId</b> member.  If the 
     <b>QueryType</b> member is set to <b>PropertyExistsQuery</b>, then no 
     structure is returned.




## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566346">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566968">STORAGE_DESCRIPTOR_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566971">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566996">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566998">STORAGE_QUERY_TYPE</a>
 

 

