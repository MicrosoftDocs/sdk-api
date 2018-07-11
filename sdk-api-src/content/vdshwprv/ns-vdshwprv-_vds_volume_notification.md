---
UID: NS:vdshwprv._VDS_VOLUME_NOTIFICATION
title: "_VDS_VOLUME_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of volume events.
old-location: base\vds_volume_notification.htm
old-project: vds
ms.assetid: 0aea3de4-60b1-4452-a5f1-f3556e719e09
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_NF_VOLUME_ARRIVE, VDS_NF_VOLUME_DEPART, VDS_NF_VOLUME_MODIFY, VDS_NF_VOLUME_REBUILDING_PROGRESS, VDS_VOLUME_NOTIFICATION, VDS_VOLUME_NOTIFICATION structure [VDS], _VDS_VOLUME_NOTIFICATION, base.vds_volume_notification, vds/_VDS_VOLUME_NOTIFICATION, vdshwprv/_VDS_VOLUME_NOTIFICATION
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
req.typenames: VDS_VOLUME_NOTIFICATION
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_VOLUME_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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
A member of the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> structure 
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



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive volume events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.

To get the volume object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/ba4a92c9-35f1-463a-8fa3-1a0d78720555">IVdsVolume::GetProperties</a> method or the <a href="https://msdn.microsoft.com/9580ceb2-6b2f-4313-a140-f6fa6a366960">IVdsVolume2::GetProperties2</a> method to get the volume properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>
 

 

