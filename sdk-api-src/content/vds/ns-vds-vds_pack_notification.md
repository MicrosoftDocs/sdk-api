---
UID: NS:vds._VDS_PACK_NOTIFICATION
title: VDS_PACK_NOTIFICATION (vds.h)
description: Defines the details of pack events.
helpviewer_keywords: ["VDS_NF_PACK_ARRIVE","VDS_NF_PACK_DEPART","VDS_NF_PACK_MODIFY","VDS_PACK_NOTIFICATION","VDS_PACK_NOTIFICATION structure [VDS]","base.vds_pack_notification","vds/_VDS_PACK_NOTIFICATION","vdshwprv/_VDS_PACK_NOTIFICATION"]
old-location: base\vds_pack_notification.htm
tech.root: base
ms.assetid: 3bfdef22-e3ad-4b23-9aaa-c2d08044dd25
ms.date: 12/05/2018
ms.keywords: VDS_NF_PACK_ARRIVE, VDS_NF_PACK_DEPART, VDS_NF_PACK_MODIFY, VDS_PACK_NOTIFICATION, VDS_PACK_NOTIFICATION structure [VDS], base.vds_pack_notification, vds/_VDS_PACK_NOTIFICATION, vdshwprv/_VDS_PACK_NOTIFICATION
f1_keywords:
- vds/VDS_PACK_NOTIFICATION
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_PACK_NOTIFICATION
targetos: Windows
req.typenames: VDS_PACK_NOTIFICATION
req.redist: 
ms.custom: 19H1
---

# VDS_PACK_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the details of pack events.


## -struct-fields




### -field ulEvent

Determines the pack event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_ARRIVE"></a><a id="vds_nf_pack_arrive"></a><dl>
<dt><b>VDS_NF_PACK_ARRIVE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A new pack arrived.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_DEPART"></a><a id="vds_nf_pack_depart"></a><dl>
<dt><b>VDS_NF_PACK_DEPART</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An existing pack was removed.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_MODIFY"></a><a id="vds_nf_pack_modify"></a><dl>
<dt><b>VDS_NF_PACK_MODIFY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a> 
       structure for the pack was changed.

</td>
</tr>
</table>
 


### -field packId

The GUID for the pack that triggered the event.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive pack events by implementing the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> method.

To get the pack object, use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">IVdsService::GetObject</a> method. You can then use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a> method to get the pack properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
 

 

