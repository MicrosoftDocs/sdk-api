---
UID: NS:vds._VDS_TARGET_NOTIFICATION
title: VDS_TARGET_NOTIFICATION (vds.h)
description: The VDS_TARGET_NOTIFICATION structure (vds.h) defines the details of iSCSI target events.
helpviewer_keywords: ["VDS_NF_TARGET_ARRIVE","VDS_NF_TARGET_DEPART","VDS_NF_TARGET_MODIFY","VDS_TARGET_NOTIFICATION","VDS_TARGET_NOTIFICATION structure [VDS]","base.vds_target_notification","vds/_VDS_TARGET_NOTIFICATION","vdshwprv/_VDS_TARGET_NOTIFICATION"]
old-location: base\vds_target_notification.htm
tech.root: base
ms.assetid: 71453c9c-d6a7-4527-8988-c0388d7a9991
ms.date: 08/05/2022
ms.keywords: VDS_NF_TARGET_ARRIVE, VDS_NF_TARGET_DEPART, VDS_NF_TARGET_MODIFY, VDS_TARGET_NOTIFICATION, VDS_TARGET_NOTIFICATION structure [VDS], base.vds_target_notification, vds/_VDS_TARGET_NOTIFICATION, vdshwprv/_VDS_TARGET_NOTIFICATION
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VDS_TARGET_NOTIFICATION
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_TARGET_NOTIFICATION
 - vds/_VDS_TARGET_NOTIFICATION
 - VDS_TARGET_NOTIFICATION
 - vds/VDS_TARGET_NOTIFICATION
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
 - VDS_TARGET_NOTIFICATION
---

# VDS_TARGET_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of iSCSI target events.

## -struct-fields

### -field ulEvent

Determines the iSCSI target event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_ARRIVE"></a><a id="vds_nf_target_arrive"></a><dl>
<dt><b>VDS_NF_TARGET_ARRIVE</b></dt>
<dt>126</dt>
</dl>
</td>
<td width="60%">
An iSCSI target has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_DEPART"></a><a id="vds_nf_target_depart"></a><dl>
<dt><b>VDS_NF_TARGET_DEPART</b></dt>
<dt>127</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI target has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_MODIFY"></a><a id="vds_nf_target_modify"></a><dl>
<dt><b>VDS_NF_TARGET_MODIFY</b></dt>
<dt>128</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI target has changed. An example of change that triggers this notification would be
        changes to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_target_prop">VDS_ISCSI_TARGET_PROP</a> 
        structure. Applications are responsible for determining the nature of any changes.

</td>
</tr>
</table>

### -field targetId

The <b>VDS_OBJECT_ID</b> of the iSCSI target that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the iSCSI target object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-getproperties">IVdsIscsiTarget::GetProperties</a> method to get the target properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_target_prop">VDS_ISCSI_TARGET_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
