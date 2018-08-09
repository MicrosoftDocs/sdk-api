---
UID: NS:vdshwprv._VDS_PARTITION_NOTIFICATION
title: "_VDS_PARTITION_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of partition events.
old-location: base\vds_partition_notification.htm
old-project: vds
ms.assetid: f731d45d-e406-4a03-a604-c6ac001c341f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_NF_PARTITION_ARRIVE, VDS_NF_PARTITION_DEPART, VDS_NF_PARTITION_MODIFY, VDS_PARTITION_NOTIFICATION, VDS_PARTITION_NOTIFICATION structure [VDS], _VDS_PARTITION_NOTIFICATION, base.vds_partition_notification, vds/_VDS_PARTITION_NOTIFICATION, vdshwprv/_VDS_PARTITION_NOTIFICATION
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
req.typenames: VDS_PARTITION_NOTIFICATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_PARTITION_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_PARTITION_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of partition events.


## -struct-fields




### -field ulEvent

Determines the partition event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_ARRIVE"></a><a id="vds_nf_partition_arrive"></a><dl>
<dt><b>VDS_NF_PARTITION_ARRIVE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
A new partition arrived. If the partition is a volume, the event also triggers a volume-arrival 
        notification.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_DEPART"></a><a id="vds_nf_partition_depart"></a><dl>
<dt><b>VDS_NF_PARTITION_DEPART</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
An existing partition was removed. If the partition is a volume, the event also triggers a 
        volume-departure notification.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PARTITION_MODIFY"></a><a id="vds_nf_partition_modify"></a><dl>
<dt><b>VDS_NF_PARTITION_MODIFY</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
A member was changed in the <a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a> 
       structure for the partition. If the partition is a volume, and if the properties of the partition have 
        changed, a <b>VDS_NF_VOLUME_MODIFY</b> notification is also sent.

</td>
</tr>
</table>
 


### -field diskId

The GUID of the disk containing the partition that triggered the event.


### -field ullOffset

The Partition offset.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive partition events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

