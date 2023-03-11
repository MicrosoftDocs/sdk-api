---
UID: NS:vds._VDS_FILE_SYSTEM_NOTIFICATION
title: VDS_FILE_SYSTEM_NOTIFICATION (vds.h)
description: The VDS_FILE_SYSTEM_NOTIFICATION structure (vds.h) defines the details of file-system events.  
helpviewer_keywords: ["VDS_FILE_SYSTEM_NOTIFICATION","VDS_FILE_SYSTEM_NOTIFICATION structure [VDS]","VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS","VDS_NF_FILE_SYSTEM_MODIFY","base.vds_file_system_notification","vds/_VDS_FILE_SYSTEM_NOTIFICATION","vdshwprv/_VDS_FILE_SYSTEM_NOTIFICATION"]
old-location: base\vds_file_system_notification.htm
tech.root: base
ms.assetid: 81d62c22-4f29-43f6-a00e-12502174a768
ms.date: 08/05/2022
ms.keywords: VDS_FILE_SYSTEM_NOTIFICATION, VDS_FILE_SYSTEM_NOTIFICATION structure [VDS], VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS, VDS_NF_FILE_SYSTEM_MODIFY, base.vds_file_system_notification, vds/_VDS_FILE_SYSTEM_NOTIFICATION, vdshwprv/_VDS_FILE_SYSTEM_NOTIFICATION
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
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_NOTIFICATION
 - vds/_VDS_FILE_SYSTEM_NOTIFICATION
 - VDS_FILE_SYSTEM_NOTIFICATION
 - vds/VDS_FILE_SYSTEM_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_FILE_SYSTEM_NOTIFICATION
---

# VDS_FILE_SYSTEM_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of file-system events.

## -struct-fields

### -field ulEvent

Determines the file-system event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_FILE_SYSTEM_MODIFY"></a><a id="vds_nf_file_system_modify"></a><dl>
<dt><b>VDS_NF_FILE_SYSTEM_MODIFY</b></dt>
<dt>203</dt>
</dl>
</td>
<td width="60%">
A member was changed in the 
       <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> structure for the file 
       system.
       For example, a volume received a new label, or a file system was extended or shrunk; does not include a change to the file-system compression flags.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS"></a><a id="vds_nf_file_system_format_progress"></a><dl>
<dt><b>VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS</b></dt>
<dt>204</dt>
</dl>
</td>
<td width="60%">
A file system volume is being formatted.

</td>
</tr>
</table>

### -field volumeId

The GUID of the volume object containing the file system that triggered the event.

### -field dwPercentCompleted

The completed format progress as a percentage of the whole.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this structure as a member.

An application can receive file-system events by implementing the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
