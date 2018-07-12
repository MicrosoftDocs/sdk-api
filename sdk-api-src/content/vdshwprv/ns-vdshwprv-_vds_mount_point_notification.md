---
UID: NS:vdshwprv._VDS_MOUNT_POINT_NOTIFICATION
title: "_VDS_MOUNT_POINT_NOTIFICATION"
author: windows-sdk-content
description: Represents notification information that was returned by the basic or dynamic software provider because a drive letter or volume GUID path changed.
old-location: base\vds_mount_point_notification.htm
old-project: vds
ms.assetid: 6e49437e-8fc7-4fc5-a227-b326a1ea9967
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_MOUNT_POINT_NOTIFICATION, VDS_MOUNT_POINT_NOTIFICATION structure [VDS], VDS_NF_MOUNT_POINTS_CHANGE, _VDS_MOUNT_POINT_NOTIFICATION, base.vds_mount_point_notification, vds/_VDS_MOUNT_POINT_NOTIFICATION, vdshwprv/_VDS_MOUNT_POINT_NOTIFICATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VDS_MOUNT_POINT_NOTIFICATION
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_MOUNT_POINT_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive these event notifications by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

