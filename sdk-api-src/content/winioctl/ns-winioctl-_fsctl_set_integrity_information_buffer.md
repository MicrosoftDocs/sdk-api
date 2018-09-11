---
UID: NS:winioctl._FSCTL_SET_INTEGRITY_INFORMATION_BUFFER
title: "_FSCTL_SET_INTEGRITY_INFORMATION_BUFFER"
author: windows-sdk-content
description: Input buffer passed with the FSCTL_SET_INTEGRITY_INFORMATION control code.
old-location: fs\fsctl_set_integrity_information_buffer.htm
tech.root: fileio
ms.assetid: e5f6c4c5-86cb-4e95-bc24-05d2bea37bc8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PFSCTL_SET_INTEGRITY_INFORMATION_BUFFER, CHECKSUM_TYPE_CRC64, CHECKSUM_TYPE_NONE, CHECKSUM_TYPE_UNCHANGED, FSCTL_INTEGRITY_FLAG_CHECKSUM_ENFORCEMENT_OFF, FSCTL_SET_INTEGRITY_INFORMATION_BUFFER, FSCTL_SET_INTEGRITY_INFORMATION_BUFFER structure [Files], PFSCTL_SET_INTEGRITY_INFORMATION_BUFFER, PFSCTL_SET_INTEGRITY_INFORMATION_BUFFER structure pointer [Files], _FSCTL_SET_INTEGRITY_INFORMATION_BUFFER, fs.fsctl_set_integrity_information_buffer, winioctl/FSCTL_SET_INTEGRITY_INFORMATION_BUFFER, winioctl/PFSCTL_SET_INTEGRITY_INFORMATION_BUFFER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FSCTL_SET_INTEGRITY_INFORMATION_BUFFER
product: Windows
targetos: Windows
req.typenames: FSCTL_SET_INTEGRITY_INFORMATION_BUFFER, *PFSCTL_SET_INTEGRITY_INFORMATION_BUFFER
req.redist: 
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
 

 

