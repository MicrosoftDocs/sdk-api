---
UID: NS:vds._VDS_DRIVE_LETTER_NOTIFICATION
title: VDS_DRIVE_LETTER_NOTIFICATION (vds.h)
description: Defines the details of drive-letter events.
helpviewer_keywords: ["VDS_DRIVE_LETTER_NOTIFICATION","VDS_DRIVE_LETTER_NOTIFICATION structure [VDS]","VDS_NF_DRIVE_LETTER_ASSIGN","VDS_NF_DRIVE_LETTER_FREE","base.vds_drive_letter_notification","vds/_VDS_DRIVE_LETTER_NOTIFICATION","vdshwprv/_VDS_DRIVE_LETTER_NOTIFICATION"]
old-location: base\vds_drive_letter_notification.htm
tech.root: base
ms.assetid: d64d1ba6-88a2-4418-b32c-36a84e973a06
ms.date: 12/05/2018
ms.keywords: VDS_DRIVE_LETTER_NOTIFICATION, VDS_DRIVE_LETTER_NOTIFICATION structure [VDS], VDS_NF_DRIVE_LETTER_ASSIGN, VDS_NF_DRIVE_LETTER_FREE, base.vds_drive_letter_notification, vds/_VDS_DRIVE_LETTER_NOTIFICATION, vdshwprv/_VDS_DRIVE_LETTER_NOTIFICATION
f1_keywords:
- vds/VDS_DRIVE_LETTER_NOTIFICATION
dev_langs:
- c++
req.header: vds.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_DRIVE_LETTER_NOTIFICATION
targetos: Windows
req.typenames: VDS_DRIVE_LETTER_NOTIFICATION
req.redist: 
ms.custom: 19H1
---

# VDS_DRIVE_LETTER_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

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



The <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive drive-letter events by implementing the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
 

 

