---
UID: NS:vdshwprv._VDS_MOUNT_POINT_NOTIFICATION
title: VDS_MOUNT_POINT_NOTIFICATION (vdshwprv.h)
description: Represents notification information that was returned by the basic or dynamic software provider because a drive letter or volume GUID path changed.helpviewer_keywords: ["VDS_MOUNT_POINT_NOTIFICATION","VDS_MOUNT_POINT_NOTIFICATION structure [VDS]","VDS_NF_MOUNT_POINTS_CHANGE","base.vds_mount_point_notification","vds/_VDS_MOUNT_POINT_NOTIFICATION","vdshwprv/_VDS_MOUNT_POINT_NOTIFICATION"]
old-location: base\vds_mount_point_notification.htm
tech.root: VDS
ms.assetid: 6e49437e-8fc7-4fc5-a227-b326a1ea9967
ms.date: 12/05/2018
ms.keywords: VDS_MOUNT_POINT_NOTIFICATION, VDS_MOUNT_POINT_NOTIFICATION structure [VDS], VDS_NF_MOUNT_POINTS_CHANGE, base.vds_mount_point_notification, vds/_VDS_MOUNT_POINT_NOTIFICATION, vdshwprv/_VDS_MOUNT_POINT_NOTIFICATION
f1_keywords:
- vdshwprv/VDS_MOUNT_POINT_NOTIFICATION
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_MOUNT_POINT_NOTIFICATION
targetos: Windows
req.typenames: VDS_MOUNT_POINT_NOTIFICATION
req.redist: 
ms.custom: 19H1
---

# VDS_MOUNT_POINT_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Represents notification information that was returned by the basic or dynamic software provider because a drive letter  or volume GUID path changed.


## -struct-fields




### -field ulEvent

Determines the event for which an application will be notified, as the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_MOUNT_POINTS_CHANGE"></a><a id="vds_nf_mount_points_change"></a><dl>
<dt><b>VDS_NF_MOUNT_POINTS_CHANGE</b></dt>
<dt>205</dt>
</dl>
</td>
<td width="60%">
The drive letter  or volume GUID path changed.

</td>
</tr>
</table>
 


### -field volumeId

The GUID of the volume object associated with the drive letter or volume GUID path that triggered the event.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive these event notifications by implementing the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a> 
    method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">IVdsService::Advise</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_notification">VDS_NOTIFICATION</a>
 

 

