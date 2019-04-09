---
UID: NS:vds._VDS_DISK_NOTIFICATION
title: VDS_DISK_NOTIFICATION (vds.h)
author: windows-sdk-content
description: Defines the details of disk events.
old-location: base\vds_disk_notification.htm
tech.root: VDS
ms.assetid: ff0069ce-611f-4ad4-9b67-adb7dc0f7abc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_DISK_NOTIFICATION, VDS_DISK_NOTIFICATION structure [VDS], VDS_NF_DISK_ARRIVE, VDS_NF_DISK_DEPART, VDS_NF_DISK_MODIFY, base.vds_disk_notification, vds/_VDS_DISK_NOTIFICATION, vdshwprv/_VDS_DISK_NOTIFICATION
ms.topic: struct
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
 - VDS_DISK_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_DISK_NOTIFICATION
req.redist: 
---

# VDS_DISK_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the details of disk events.


## -struct-fields




### -field ulEvent

Determines the disk event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_ARRIVE"></a><a id="vds_nf_disk_arrive"></a><dl>
<dt><b>VDS_NF_DISK_ARRIVE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
A disk was inserted, or a RAID controller surfaced a LUN that is local to the host.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_DEPART"></a><a id="vds_nf_disk_depart"></a><dl>
<dt><b>VDS_NF_DISK_DEPART</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
A disk was removed, or a RAID controller unbound a LUN.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_DISK_MODIFY"></a><a id="vds_nf_disk_modify"></a><dl>
<dt><b>VDS_NF_DISK_MODIFY</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
A member of the 
       <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> structure changed, or an extent on a 
        disk changed.

</td>
</tr>
</table>
 


### -field diskId

The GUID of the disk object that triggered the event.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.

To get the disk object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a> method or the <a href="https://msdn.microsoft.com/ef88b61b-9139-4767-b54f-46122650e922">IVdsDisk3::GetProperties2</a> method to get the disk properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

