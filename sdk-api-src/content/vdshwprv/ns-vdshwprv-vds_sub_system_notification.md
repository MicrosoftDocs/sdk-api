---
UID: NS:vdshwprv._VDS_SUB_SYSTEM_NOTIFICATION
title: VDS_SUB_SYSTEM_NOTIFICATION (vdshwprv.h)
description: The VDS_SUB_SYSTEM_NOTIFICATION structure (vdshwprv.h) defines the details of subsystem events.
helpviewer_keywords: ["VDS_NF_SUB_SYSTEM_ARRIVE","VDS_NF_SUB_SYSTEM_DEPART","VDS_NF_SUB_SYSTEM_MODIFY","VDS_SUB_SYSTEM_NOTIFICATION","VDS_SUB_SYSTEM_NOTIFICATION structure [VDS]","base.vds_sub_system_notification","vds/_VDS_SUB_SYSTEM_NOTIFICATION","vdshwprv/_VDS_SUB_SYSTEM_NOTIFICATION"]
old-location: base\vds_sub_system_notification.htm
tech.root: base
ms.assetid: 368e5b3d-11ba-400e-8dd0-929d45199dd9
ms.date: 08/09/2022
ms.keywords: VDS_NF_SUB_SYSTEM_ARRIVE, VDS_NF_SUB_SYSTEM_DEPART, VDS_NF_SUB_SYSTEM_MODIFY, VDS_SUB_SYSTEM_NOTIFICATION, VDS_SUB_SYSTEM_NOTIFICATION structure [VDS], base.vds_sub_system_notification, vds/_VDS_SUB_SYSTEM_NOTIFICATION, vdshwprv/_VDS_SUB_SYSTEM_NOTIFICATION
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
req.typenames: VDS_SUB_SYSTEM_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_SUB_SYSTEM_NOTIFICATION
 - vdshwprv/_VDS_SUB_SYSTEM_NOTIFICATION
 - VDS_SUB_SYSTEM_NOTIFICATION
 - vdshwprv/VDS_SUB_SYSTEM_NOTIFICATION
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
 - VDS_SUB_SYSTEM_NOTIFICATION
---

# VDS_SUB_SYSTEM_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the details of subsystem events.

## -struct-fields

### -field ulEvent

Determines the subsystem event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_ARRIVE"></a><a id="vds_nf_sub_system_arrive"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_ARRIVE</b></dt>
<dt>101</dt>
</dl>
</td>
<td width="60%">
A new subsystem was connected to the server or network.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_DEPART"></a><a id="vds_nf_sub_system_depart"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_DEPART</b></dt>
<dt>102</dt>
</dl>
</td>
<td width="60%">
An existing subsystem was disconnected.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_MODIFY"></a><a id="vds_nf_sub_system_modify"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_MODIFY</b></dt>
<dt>151</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> 
        structure was changed.

</td>
</tr>
</table>

### -field subSystemId

The subsystem's GUID.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive subsystem events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

To get the subsystem object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a> method or the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem2-getproperties2">IVdsSubSystem2::GetProperties2</a> methodto get the subsystem properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a>
