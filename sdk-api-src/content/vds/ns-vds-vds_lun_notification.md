---
UID: NS:vds._VDS_LUN_NOTIFICATION
title: VDS_LUN_NOTIFICATION (vds.h)
description: The VDS_LUN_NOTIFICATION structure (vds.h) defines the details of a LUN notification.
helpviewer_keywords: ["VDS_LUN_NOTIFICATION","VDS_LUN_NOTIFICATION structure [VDS]","VDS_NF_LUN_ARRIVE","VDS_NF_LUN_DEPART","VDS_NF_LUN_MODIFY","base.vds_lun_notification","vds/_VDS_LUN_NOTIFICATION","vdshwprv/_VDS_LUN_NOTIFICATION"]
old-location: base\vds_lun_notification.htm
tech.root: base
ms.assetid: 42b71b32-337e-4352-b4b3-6af2caad86e5
ms.date: 08/05/2022
ms.keywords: VDS_LUN_NOTIFICATION, VDS_LUN_NOTIFICATION structure [VDS], VDS_NF_LUN_ARRIVE, VDS_NF_LUN_DEPART, VDS_NF_LUN_MODIFY, base.vds_lun_notification, vds/_VDS_LUN_NOTIFICATION, vdshwprv/_VDS_LUN_NOTIFICATION
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
req.typenames: VDS_LUN_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_NOTIFICATION
 - vds/_VDS_LUN_NOTIFICATION
 - VDS_LUN_NOTIFICATION
 - vds/VDS_LUN_NOTIFICATION
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
 - VDS_LUN_NOTIFICATION
---

# VDS_LUN_NOTIFICATION structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the details of a LUN notification.

## -struct-fields

### -field ulEvent

Determines the LUN event for which an application will be notified, as one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_ARRIVE"></a><a id="vds_nf_lun_arrive"></a><dl>
<dt><b>VDS_NF_LUN_ARRIVE</b></dt>
<dt>108</dt>
</dl>
</td>
<td width="60%">
A new LUN has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_DEPART"></a><a id="vds_nf_lun_depart"></a><dl>
<dt><b>VDS_NF_LUN_DEPART</b></dt>
<dt>109</dt>
</dl>
</td>
<td width="60%">
An existing LUN has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_MODIFY"></a><a id="vds_nf_lun_modify"></a><dl>
<dt><b>VDS_NF_LUN_MODIFY</b></dt>
<dt>110</dt>
</dl>
</td>
<td width="60%">
A member was changed in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_prop">VDS_LUN_PROP</a> 
       structure for an external LUN. Examples of changes that trigger this notification include changes to the 
       <b>VDS_LUN_PROP</b> structure and the addition of a plex to 
        the LUN. Applications are responsible for determining the precise nature of the change.

</td>
</tr>
</table>

### -field LunId

The GUID of the LUN.

## -remarks

This structure is included as a member in the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure.

An application can receive LUN events by implementing the 
    <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

To get the LUN object, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">IVdsLun::GetProperties</a> method to get the LUN properties.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
