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

# _FSCTL_SET_INTEGRITY_INFORMATION_BUFFER structure


## -description


Input buffer passed with the 
     <a href="https://msdn.microsoft.com/bd5be96d-6fdc-4fad-9d01-81b913a5b653">FSCTL_SET_INTEGRITY_INFORMATION</a> control 
     code.


## -struct-fields




### -field ChecksumAlgorithm

Specifies the checksum algorithm.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CHECKSUM_TYPE_NONE"></a><a id="checksum_type_none"></a><dl>
<dt><b>CHECKSUM_TYPE_NONE</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
The file or directory is not configured to use integrity.

</td>
</tr>
<tr>
<td width="40%"><a id="CHECKSUM_TYPE_CRC64"></a><a id="checksum_type_crc64"></a><dl>
<dt><b>CHECKSUM_TYPE_CRC64</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The file or directory uses a CRC64 checksum to provide integrity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3–0xfffe</dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Must not be used.

</td>
</tr>
<tr>
<td width="40%"><a id="CHECKSUM_TYPE_UNCHANGED"></a><a id="checksum_type_unchanged"></a><dl>
<dt><b>CHECKSUM_TYPE_UNCHANGED</b></dt>
<dt>0xffff</dt>
</dl>
</td>
<td width="60%">
The checksum algorithm is to remain the same.

</td>
</tr>
</table>
 


### -field Reserved

Must be 0


### -field Flags

Contains zero or more flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF"></a><a id="fsctl_integrity_flag_checksum_enforcement_off"></a><dl>
<dt><b>FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If set, the checksum enforcement is disabled and reads will succeed even if the checksums do not match. 
        This flag is valid only if the file has an integrity algorithm  set. If there is no algorithm set or the 
        <b>CheckSum</b> member is set to <b>CHECKSUM_TYPE_NONE</b>, then the 
        operation fails with <b>ERROR_INVALID_PARAMETER</b>.

</td>
</tr>
</table>
 


## -remarks



If <b>FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF</b> is specified and the file is opened 
    with sharing permissions such that subsequent opens can succeed, it's possible for corrupt data to be read by an 
    application that did not specify <b>FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF</b>.




## -see-also




<a href="https://msdn.microsoft.com/ab87f987-b734-4ad0-af16-1ba967db48d7">FSCTL_GET_INTEGRITY_INFORMATION_BUFFER</a>



<a href="https://msdn.microsoft.com/bd5be96d-6fdc-4fad-9d01-81b913a5b653">FSCTL_SET_INTEGRITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

