---
UID: NS:vds._VDS_DISK_NOTIFICATION
title: VDS_DISK_NOTIFICATION (vds.h)
description: The VDS_DISK_NOTIFICATION structure (vds.h) defines the details of disk events. 
helpviewer_keywords: ["VDS_DISK_NOTIFICATION","VDS_DISK_NOTIFICATION structure [VDS]","VDS_NF_DISK_ARRIVE","VDS_NF_DISK_DEPART","VDS_NF_DISK_MODIFY","base.vds_disk_notification","vds/_VDS_DISK_NOTIFICATION","vdshwprv/_VDS_DISK_NOTIFICATION"]
old-location: base\vds_disk_notification.htm
tech.root: base
ms.assetid: ff0069ce-611f-4ad4-9b67-adb7dc0f7abc
ms.date: 08/05/2022
ms.keywords: VDS_DISK_NOTIFICATION, VDS_DISK_NOTIFICATION structure [VDS], VDS_NF_DISK_ARRIVE, VDS_NF_DISK_DEPART, VDS_NF_DISK_MODIFY, base.vds_disk_notification, vds/_VDS_DISK_NOTIFICATION, vdshwprv/_VDS_DISK_NOTIFICATION
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
req.typenames: VDS_DISK_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_NOTIFICATION
 - vds/_VDS_DISK_NOTIFICATION
 - VDS_DISK_NOTIFICATION
 - vds/VDS_DISK_NOTIFICATION
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
 - VDS_DISK_NOTIFICATION
---

# VDS_DISK_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the details of disk events.

## -struct-fields

### -field ulEvent

Determines the disk event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_ARRIVE"></a><a id="vds_nf_disk_arrive"></a><dl>
<dt><b>VDS_NF_DISK_ARRIVE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
A disk was inserted, or a RAID controller surfaced a LUN that is local to the host.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_DEPART"></a><a id="vds_nf_disk_depart"></a><dl>
<dt><b>VDS_NF_DISK_DEPART</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
A disk was removed, or a RAID controller unbound a LUN.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_MODIFY"></a><a id="vds_nf_disk_modify"></a><dl>
<dt><b>VDS_NF_DISK_MODIFY</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
A member of the 
       <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure changed, or an extent on a 
        disk changed.

</td>
</tr>
</table>

### -field diskId

The GUID of the disk object that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the disk object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> method or the <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a> method to get the disk properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
