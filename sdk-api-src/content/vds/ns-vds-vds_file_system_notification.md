---
UID: NS:vds._VDS_FILE_SYSTEM_NOTIFICATION
title: VDS_FILE_SYSTEM_NOTIFICATION
author: windows-sdk-content
description: Defines the details of file-system events.
old-location: base\vds_file_system_notification.htm
tech.root: vds
ms.assetid: 81d62c22-4f29-43f6-a00e-12502174a768
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_FILE_SYSTEM_NOTIFICATION, VDS_FILE_SYSTEM_NOTIFICATION structure [VDS], VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS, VDS_NF_FILE_SYSTEM_MODIFY, base.vds_file_system_notification, vds/_VDS_FILE_SYSTEM_NOTIFICATION, vdshwprv/_VDS_FILE_SYSTEM_NOTIFICATION
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
 - VDS_FILE_SYSTEM_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_NOTIFICATION
req.redist: 
---

# VDS_FILE_SYSTEM_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of file-system events.


## -struct-fields




### -field ulEvent

Determines the file-system event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_FILE_SYSTEM_MODIFY"></a><a id="vds_nf_file_system_modify"></a><dl>
<dt><b>VDS_NF_FILE_SYSTEM_MODIFY</b></dt>
<dt>203</dt>
</dl>
</td>
<td width="60%">
A member was changed in the 
       <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> structure for the file 
       system.
       For example, a volume received a new label, or a file system was extended or shrunk; does not include a change to the file-system compression flags.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS"></a><a id="vds_nf_file_system_format_progress"></a><dl>
<dt><b>VDS_NF_FILE_SYSTEM_FORMAT_PROGRESS</b></dt>
<dt>204</dt>
</dl>
</td>
<td width="60%">
A file system volume is being formatted.

</td>
</tr>
</table>
 


### -field volumeId

The GUID of the volume object containing the file system that triggered the event.


### -field dwPercentCompleted

The completed format progress as a percentage of the whole.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this structure as a member.

An application can receive file-system events by implementing the <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

