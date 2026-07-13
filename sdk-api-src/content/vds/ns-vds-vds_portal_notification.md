---
UID: NS:vds._VDS_PORTAL_NOTIFICATION
title: VDS_PORTAL_NOTIFICATION (vds.h)
description: The VDS_PORTAL_NOTIFICATION structure (vds.h) defines the details of iSCSI portal events.
helpviewer_keywords: ["VDS_NF_PORTAL_ARRIVE","VDS_NF_PORTAL_DEPART","VDS_NF_PORTAL_MODIFY","VDS_PORTAL_NOTIFICATION","VDS_PORTAL_NOTIFICATION structure [VDS]","base.vds_portal_notification","vds/_VDS_PORTAL_NOTIFICATION","vdshwprv/_VDS_PORTAL_NOTIFICATION"]
old-location: base\vds_portal_notification.htm
tech.root: base
ms.assetid: 53126339-a9b7-4b80-80af-ac1782dff8a8
ms.date: 08/05/2022
ms.keywords: VDS_NF_PORTAL_ARRIVE, VDS_NF_PORTAL_DEPART, VDS_NF_PORTAL_MODIFY, VDS_PORTAL_NOTIFICATION, VDS_PORTAL_NOTIFICATION structure [VDS], base.vds_portal_notification, vds/_VDS_PORTAL_NOTIFICATION, vdshwprv/_VDS_PORTAL_NOTIFICATION
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
req.typenames: VDS_PORTAL_NOTIFICATION
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_PORTAL_NOTIFICATION
 - vds/_VDS_PORTAL_NOTIFICATION
 - VDS_PORTAL_NOTIFICATION
 - vds/VDS_PORTAL_NOTIFICATION
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
 - VDS_PORTAL_NOTIFICATION
---

# VDS_PORTAL_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of iSCSI portal events.

## -struct-fields

### -field ulEvent

Determines the iSCSI portal event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_ARRIVE"></a><a id="vds_nf_portal_arrive"></a><dl>
<dt><b>VDS_NF_PORTAL_ARRIVE</b></dt>
<dt>123</dt>
</dl>
</td>
<td width="60%">
An iSCSI portal has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_DEPART"></a><a id="vds_nf_portal_depart"></a><dl>
<dt><b>VDS_NF_PORTAL_DEPART</b></dt>
<dt>124</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal has been removed.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_MODIFY"></a><a id="vds_nf_portal_modify"></a><dl>
<dt><b>VDS_NF_PORTAL_MODIFY</b></dt>
<dt>125</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal has changed. An example of change that triggers this notification would be
        changes to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portal_prop">VDS_ISCSI_PORTAL_PROP</a> 
        structure. Applications are responsible for determining the nature of any changes.

</td>
</tr>
</table>

### -field portalId

The <b>VDS_OBJECT_ID</b> of the iSCSI portal that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the portal object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getproperties">IVdsIscsiPortal::GetProperties</a> method to get the portal properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsiportal">IVdsIscsiPortal</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portal_prop">VDS_ISCSI_PORTAL_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
