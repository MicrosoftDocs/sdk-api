---
UID: NS:vdshwprv._VDS_DRIVE_LETTER_NOTIFICATION
title: "_VDS_DRIVE_LETTER_NOTIFICATION"
author: windows-driver-content
description: Defines the details of drive-letter events.
old-location: base\vds_drive_letter_notification.htm
old-project: VDS
ms.assetid: d64d1ba6-88a2-4418-b32c-36a84e973a06
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VDS_DRIVE_LETTER_NOTIFICATION, VDS_DRIVE_LETTER_NOTIFICATION structure [VDS], VDS_NF_DRIVE_LETTER_ASSIGN, VDS_NF_DRIVE_LETTER_FREE, _VDS_DRIVE_LETTER_NOTIFICATION, base.vds_drive_letter_notification, vds/_VDS_DRIVE_LETTER_NOTIFICATION, vdshwprv/_VDS_DRIVE_LETTER_NOTIFICATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: VDS_DRIVE_LETTER_NOTIFICATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_DRIVE_LETTER_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_DRIVE_LETTER_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of drive-letter events.


## -struct-fields




### -field ulEvent

Determines the drive-letter event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_LETTER_FREE"></a><a id="vds_nf_drive_letter_free"></a><dl>
<dt><b>VDS_NF_DRIVE_LETTER_FREE</b></dt>
<dt>201</dt>
</dl>
</td>
<td width="60%">
The drive letter of an uninitialized disk is free.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DRIVE_LETTER_ASSIGN"></a><a id="vds_nf_drive_letter_assign"></a><dl>
<dt><b>VDS_NF_DRIVE_LETTER_ASSIGN</b></dt>
<dt>202</dt>
</dl>
</td>
<td width="60%">
The drive letter of an uninitialized disk is assigned.

</td>
</tr>
</table>
 


### -field wcLetter

The drive letter that triggered the event.


### -field volumeId

The GUID of the volume to which the drive letter is assigned. If the drive letter is freed, the volume 
      identifier is GUID_NULL.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive drive-letter events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

