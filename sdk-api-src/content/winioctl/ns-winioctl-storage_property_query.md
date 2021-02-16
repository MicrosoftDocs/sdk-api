---
UID: NS:winioctl._STORAGE_PROPERTY_QUERY
title: STORAGE_PROPERTY_QUERY
description: Indicates the properties of a storage device or adapter to retrieve as the input buffer passed to the IOCTL_STORAGE_QUERY_PROPERTY control code.
helpviewer_keywords: ["*PSTORAGE_PROPERTY_QUERY","PSTORAGE_PROPERTY_QUERY","PSTORAGE_PROPERTY_QUERY structure pointer [Files]","PropertyExistsQuery","PropertyStandardQuery","STORAGE_PROPERTY_QUERY","STORAGE_PROPERTY_QUERY structure [Files]","fs.storage_property_query","winioctl/PSTORAGE_PROPERTY_QUERY","winioctl/STORAGE_PROPERTY_QUERY"]
old-location: fs\storage_property_query.htm
tech.root: fs
ms.assetid: c97a14ab-628c-41f1-96c3-0f47654d0606
ms.date: 12/05/2018
ms.keywords: '*PSTORAGE_PROPERTY_QUERY, PSTORAGE_PROPERTY_QUERY, PSTORAGE_PROPERTY_QUERY structure pointer [Files], PropertyExistsQuery, PropertyStandardQuery, STORAGE_PROPERTY_QUERY, STORAGE_PROPERTY_QUERY structure [Files], fs.storage_property_query, winioctl/PSTORAGE_PROPERTY_QUERY, winioctl/STORAGE_PROPERTY_QUERY'
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
targetos: Windows
req.typenames: STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY
req.redist: 
f1_keywords:
 - _STORAGE_PROPERTY_QUERY
 - winioctl/_STORAGE_PROPERTY_QUERY
 - PSTORAGE_PROPERTY_QUERY
 - winioctl/PSTORAGE_PROPERTY_QUERY
 - STORAGE_PROPERTY_QUERY
 - winioctl/STORAGE_PROPERTY_QUERY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - STORAGE_PROPERTY_QUERY
---

# STORAGE_PROPERTY_QUERY structure


## -description

Indicates the properties of a storage device or adapter to retrieve as the input buffer passed to the 
   <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code.

## -struct-fields

### -field PropertyId

Indicates whether the caller is requesting a device descriptor, an adapter descriptor, a write cache 
      property, a device unique ID (DUID), or the device identifiers provided in the device's SCSI vital product data 
      (VPD) page. For a list of the property IDs that can be assigned to this member, see 
      <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>.

### -field QueryType

Contains flags indicating the type of query to be performed as enumerated by the 
      <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_query_type">STORAGE_QUERY_TYPE</a> enumeration.

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
     <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> control code can 
     be one of several structures depending on the value of the <b>PropertyId</b> member.  If the 
     <b>QueryType</b> member is set to <b>PropertyExistsQuery</b>, then no 
     structure is returned.

## -see-also

<a href="/windows/desktop/FileIO/disk-management-structures">Disk Management Structures</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_adapter_descriptor">STORAGE_ADAPTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_descriptor_header">STORAGE_DESCRIPTOR_HEADER</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor">STORAGE_DEVICE_DESCRIPTOR</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-storage_query_type">STORAGE_QUERY_TYPE</a>