---
UID: NS:vdshwprv._VDS_PARTITION_NOTIFICATION
title: VDS_PARTITION_NOTIFICATION (vdshwprv.h)
description: The VDS_PARTITION_NOTIFICATION structure (vdshwprv.h) defines the details of partition events.
helpviewer_keywords: ["VDS_NF_PARTITION_ARRIVE","VDS_NF_PARTITION_DEPART","VDS_NF_PARTITION_MODIFY","VDS_PARTITION_NOTIFICATION","VDS_PARTITION_NOTIFICATION structure [VDS]","base.vds_partition_notification","vds/_VDS_PARTITION_NOTIFICATION","vdshwprv/_VDS_PARTITION_NOTIFICATION"]
old-location: base\vds_partition_notification.htm
tech.root: base
ms.assetid: f731d45d-e406-4a03-a604-c6ac001c341f
ms.date: 08/08/2022
ms.keywords: VDS_NF_PARTITION_ARRIVE, VDS_NF_PARTITION_DEPART, VDS_NF_PARTITION_MODIFY, VDS_PARTITION_NOTIFICATION, VDS_PARTITION_NOTIFICATION structure [VDS], base.vds_partition_notification, vds/_VDS_PARTITION_NOTIFICATION, vdshwprv/_VDS_PARTITION_NOTIFICATION
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_PARTITION_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PARTITION_NOTIFICATION
 - vdshwprv/_VDS_PARTITION_NOTIFICATION
 - VDS_PARTITION_NOTIFICATION
 - vdshwprv/VDS_PARTITION_NOTIFICATION
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
 - VDS_PARTITION_NOTIFICATION
---

# VDS_PARTITION_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of partition events.

## -struct-fields

### -field ulEvent

Determines the partition event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_ARRIVE"></a><a id="vds_nf_partition_arrive"></a><dl>
<dt><b>VDS_NF_PARTITION_ARRIVE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
A new partition arrived. If the partition is a volume, the event also triggers a volume-arrival 
        notification.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_DEPART"></a><a id="vds_nf_partition_depart"></a><dl>
<dt><b>VDS_NF_PARTITION_DEPART</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
An existing partition was removed. If the partition is a volume, the event also triggers a 
        volume-departure notification.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_MODIFY"></a><a id="vds_nf_partition_modify"></a><dl>
<dt><b>VDS_NF_PARTITION_MODIFY</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
A member was changed in the <a href="/windows/desktop/api/vds/ns-vds-vds_partition_prop">VDS_PARTITION_PROP</a> 
       structure for the partition. If the partition is a volume, and if the properties of the partition have 
        changed, a <b>VDS_NF_VOLUME_MODIFY</b> notification is also sent.

</td>
</tr>
</table>

### -field diskId

The GUID of the disk containing the partition that triggered the event.

### -field ullOffset

The Partition offset.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive partition events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
