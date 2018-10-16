---
UID: NS:winioctl._STORAGE_PROPERTY_QUERY
title: "_STORAGE_PROPERTY_QUERY"
author: windows-sdk-content
description: Indicates the properties of a storage device or adapter to retrieve as the input buffer passed to the IOCTL_STORAGE_QUERY_PROPERTY control code.
old-location: fs\storage_property_query.htm
tech.root: fileio
ms.assetid: c97a14ab-628c-41f1-96c3-0f47654d0606
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PSTORAGE_PROPERTY_QUERY, PSTORAGE_PROPERTY_QUERY, PSTORAGE_PROPERTY_QUERY structure pointer [Files], PropertyExistsQuery, PropertyStandardQuery, STORAGE_PROPERTY_QUERY, STORAGE_PROPERTY_QUERY structure [Files], _STORAGE_PROPERTY_QUERY, fs.storage_property_query, winioctl/PSTORAGE_PROPERTY_QUERY, winioctl/STORAGE_PROPERTY_QUERY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WinIoCtl.h
api_name:
 - STORAGE_PROPERTY_QUERY
product: Windows
targetos: Windows
req.typenames: STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY
req.redist: 
---

# _STORAGE_PROPERTY_QUERY structure


## -description


Indicates the properties of a storage device or adapter to retrieve as the input buffer passed to the 
   <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> control code.


## -struct-fields




### -field PropertyId

Indicates whether the caller is requesting a device descriptor, an adapter descriptor, a write cache 
      property, a device unique ID (DUID), or the device identifiers provided in the device's SCSI vital product data 
      (VPD) page. For a list of the property IDs that can be assigned to this member, see 
      <a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>.


### -field QueryType

Contains flags indicating the type of query to be performed as enumerated by the 
      <a href="https://msdn.microsoft.com/0bce42d2-9d42-4881-9e33-4b3858a40353">STORAGE_QUERY_TYPE</a> enumeration.

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
     <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> control code can 
     be one of several structures depending on the value of the <b>PropertyId</b> member.  If the 
     <b>QueryType</b> member is set to <b>PropertyExistsQuery</b>, then no 
     structure is returned.




## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/8a5059d3-09a4-4411-8d86-d1257edb409a">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f98e53d5-45cb-4c3f-b04d-8eecd98655d2">STORAGE_DESCRIPTOR_HEADER</a>



<a href="https://msdn.microsoft.com/f84f8a88-b6fc-4b22-b858-52955c8d537d">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/0bce42d2-9d42-4881-9e33-4b3858a40353">STORAGE_QUERY_TYPE</a>
 

 

