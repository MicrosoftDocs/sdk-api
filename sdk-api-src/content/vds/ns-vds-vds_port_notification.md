---
UID: NS:vds._VDS_PORT_NOTIFICATION
title: VDS_PORT_NOTIFICATION (vds.h)
description: The VDS_PORT_NOTIFICATION structure (vds.h) defines the details of controller port events. 
helpviewer_keywords: ["VDS_NF_PORT_ARRIVE","VDS_NF_PORT_DEPART","VDS_NF_PORT_MODIFY","VDS_NF_PORT_REMOVED","VDS_PORT_NOTIFICATION","VDS_PORT_NOTIFICATION structure [VDS]","base.vds_port_notification","vds/_VDS_PORT_NOTIFICATION","vdshwprv/_VDS_PORT_NOTIFICATION"]
old-location: base\vds_port_notification.htm
tech.root: base
ms.assetid: 4de0969f-fed5-42c7-a5f8-0bd6c58dc237
ms.date: 08/05/2022
ms.keywords: VDS_NF_PORT_ARRIVE, VDS_NF_PORT_DEPART, VDS_NF_PORT_MODIFY, VDS_NF_PORT_REMOVED, VDS_PORT_NOTIFICATION, VDS_PORT_NOTIFICATION structure [VDS], base.vds_port_notification, vds/_VDS_PORT_NOTIFICATION, vdshwprv/_VDS_PORT_NOTIFICATION
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
req.typenames: VDS_PORT_NOTIFICATION
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_PORT_NOTIFICATION
 - vds/_VDS_PORT_NOTIFICATION
 - VDS_PORT_NOTIFICATION
 - vds/VDS_PORT_NOTIFICATION
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
 - VDS_PORT_NOTIFICATION
---

# VDS_PORT_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the details of controller port events.

## -struct-fields

### -field ulEvent

Determines the controller port event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_ARRIVE"></a><a id="vds_nf_port_arrive"></a><dl>
<dt><b>VDS_NF_PORT_ARRIVE</b></dt>
<dt>121</dt>
</dl>
</td>
<td width="60%">
A controller port is reported as physically present on the subsystem. 
The <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a> value associated with this notification should be any value except <b>VDS_PRS_REMOVED</b>.


</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_DEPART"></a><a id="vds_nf_port_depart"></a><dl>
<dt><b>VDS_NF_PORT_DEPART</b></dt>
<dt>122</dt>
</dl>
</td>
<td width="60%">
A controller, and therefore its port, were physically unplugged from the subsystem. The <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a> value should be <b>VDS_PRS_UNKNOWN</b> or <b>VDS_PRS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_MODIFY"></a><a id="vds_nf_port_modify"></a><dl>
<dt><b>VDS_NF_PORT_MODIFY</b></dt>
<dt>352</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_port_prop">VDS_PORT_PROP</a> structure changed.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_REMOVED"></a><a id="vds_nf_port_removed"></a><dl>
<dt><b>VDS_NF_PORT_REMOVED</b></dt>
<dt>353</dt>
</dl>
</td>
<td width="60%">
A controller port is physically present but not available for use. For example, either the controller or the port itself is set to inactive. The <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_port_status">VDS_PORT_STATUS</a> value should be <b>VDS_PRS_FAILED</b>  (removed from use because of failure), <b>VDS_PRS_OFFLINE</b>  (not failed, but not in use either), <b>VDS_PRS_NOT_READY</b>, or <b>VDS_PRS_UNKNOWN</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.

</td>
</tr>
</table>

### -field portId

The <b>VDS_OBJECT_ID</b> of the controller port that triggered the event.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.

To get the port object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-getproperties">IVdsControllerPort::GetProperties</a> method to get the port properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollerport">IVdsControllerPort</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
