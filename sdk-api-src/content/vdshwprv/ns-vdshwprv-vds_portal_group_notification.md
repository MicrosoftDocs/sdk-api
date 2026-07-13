---
UID: NS:vdshwprv._VDS_PORTAL_GROUP_NOTIFICATION
title: VDS_PORTAL_GROUP_NOTIFICATION (vdshwprv.h)
description: The VDS_PORTAL_GROUP_NOTIFICATION structure (vdshwprv.h) defines the details of iSCSI portal events.
helpviewer_keywords: ["VDS_NF_PORTAL_GROUP_ARRIVE","VDS_NF_PORTAL_GROUP_DEPART","VDS_NF_PORTAL_GROUP_MODIFY","VDS_PORTAL_GROUP_NOTIFICATION","VDS_PORTAL_GROUP_NOTIFICATION structure [VDS]","base.vds_portal_group_notification","vds/_VDS_PORTAL_GROUP_NOTIFICATION","vdshwprv/_VDS_PORTAL_GROUP_NOTIFICATION"]
old-location: base\vds_portal_group_notification.htm
tech.root: base
ms.assetid: db4f947b-996f-4aa0-aed6-0190f00ca58a
ms.date: 08/08/2022
ms.keywords: VDS_NF_PORTAL_GROUP_ARRIVE, VDS_NF_PORTAL_GROUP_DEPART, VDS_NF_PORTAL_GROUP_MODIFY, VDS_PORTAL_GROUP_NOTIFICATION, VDS_PORTAL_GROUP_NOTIFICATION structure [VDS], base.vds_portal_group_notification, vds/_VDS_PORTAL_GROUP_NOTIFICATION, vdshwprv/_VDS_PORTAL_GROUP_NOTIFICATION
req.header: vdshwprv.h
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
req.typenames: VDS_PORTAL_GROUP_NOTIFICATION
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_PORTAL_GROUP_NOTIFICATION
 - vdshwprv/_VDS_PORTAL_GROUP_NOTIFICATION
 - VDS_PORTAL_GROUP_NOTIFICATION
 - vdshwprv/VDS_PORTAL_GROUP_NOTIFICATION
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
 - VDS_PORTAL_GROUP_NOTIFICATION
---

# VDS_PORTAL_GROUP_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of iSCSI portal events.

## -struct-fields

### -field ulEvent

Determines the iSCSI portal group event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_ARRIVE"></a><a id="vds_nf_portal_group_arrive"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_ARRIVE</b></dt>
<dt>129</dt>
</dl>
</td>
<td width="60%">
An iSCSI portal group has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_DEPART"></a><a id="vds_nf_portal_group_depart"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_DEPART</b></dt>
<dt>130</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal group has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_MODIFY"></a><a id="vds_nf_portal_group_modify"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_MODIFY</b></dt>
<dt>131</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal group has changed. An example of change that triggers this notification would be 
        changes to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portalgroup_prop">VDS_ISCSI_PORTALGROUP_PROP</a> 
        structure. Applications are responsible for determining the nature of any changes.

</td>
</tr>
</table>

### -field portalGroupId

The <b>VDS_OBJECT_ID</b> of the iSCSI portal that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the portal group object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportalgroup-getproperties">IVdsIscsiPortalGroup::GetProperties</a> method to get the portal group properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsiportal">IVdsIscsiPortal</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portalgroup_prop">VDS_ISCSI_PORTALGROUP_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
