---
UID: NS:vdshwprv._VDS_VOLUME_NOTIFICATION
title: VDS_VOLUME_NOTIFICATION (vdshwprv.h)
description: The VDS_VOLUME_NOTIFICATION structure (vdshwprv.h) defines the details of volume events.
helpviewer_keywords: ["VDS_NF_VOLUME_ARRIVE","VDS_NF_VOLUME_DEPART","VDS_NF_VOLUME_MODIFY","VDS_NF_VOLUME_REBUILDING_PROGRESS","VDS_VOLUME_NOTIFICATION","VDS_VOLUME_NOTIFICATION structure [VDS]","base.vds_volume_notification","vds/_VDS_VOLUME_NOTIFICATION","vdshwprv/_VDS_VOLUME_NOTIFICATION"]
old-location: base\vds_volume_notification.htm
tech.root: base
ms.assetid: 0aea3de4-60b1-4452-a5f1-f3556e719e09
ms.date: 08/09/2022
ms.keywords: VDS_NF_VOLUME_ARRIVE, VDS_NF_VOLUME_DEPART, VDS_NF_VOLUME_MODIFY, VDS_NF_VOLUME_REBUILDING_PROGRESS, VDS_VOLUME_NOTIFICATION, VDS_VOLUME_NOTIFICATION structure [VDS], base.vds_volume_notification, vds/_VDS_VOLUME_NOTIFICATION, vdshwprv/_VDS_VOLUME_NOTIFICATION
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
req.typenames: VDS_VOLUME_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_NOTIFICATION
 - vdshwprv/_VDS_VOLUME_NOTIFICATION
 - VDS_VOLUME_NOTIFICATION
 - vdshwprv/VDS_VOLUME_NOTIFICATION
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
 - VDS_VOLUME_NOTIFICATION
---

# VDS_VOLUME_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of volume events.

## -struct-fields

### -field ulEvent

Determines the volume event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_VOLUME_ARRIVE"></a><a id="vds_nf_volume_arrive"></a><dl>
<dt><b>VDS_NF_VOLUME_ARRIVE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A new volume arrived.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_VOLUME_DEPART"></a><a id="vds_nf_volume_depart"></a><dl>
<dt><b>VDS_NF_VOLUME_DEPART</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
An existing volume was removed.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_VOLUME_MODIFY"></a><a id="vds_nf_volume_modify"></a><dl>
<dt><b>VDS_NF_VOLUME_MODIFY</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure 
        changed. This value can also indicate a change in one of the plexes associated with the volume, such as 
       the addition, removal, or repair of a plex.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_VOLUME_REBUILDING_PROGRESS"></a><a id="vds_nf_volume_rebuilding_progress"></a><dl>
<dt><b>VDS_NF_VOLUME_REBUILDING_PROGRESS</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
A volume is being rebuilt.

</td>
</tr>
</table>

### -field volumeId

The <b>VDS_OBJECT_ID</b> of the volume that triggered the event.

### -field plexId

The <b>VDS_OBJECT_ID</b> of a volume plex. VDS applies this identifier during the 
      rebuild operation, which can execute on multiple plexes at different rates.

### -field ulPercentCompleted

The degree to which the operation is complete.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive volume events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the volume object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a> method or the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume2-getproperties2">IVdsVolume2::GetProperties2</a> method to get the volume properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a>
