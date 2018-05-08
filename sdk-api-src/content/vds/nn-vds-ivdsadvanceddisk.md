---
UID: NN:vds.IVdsAdvancedDisk
title: IVdsAdvancedDisk
author: windows-driver-content
description: Creates and deletes partitions, and modifies partition attributes.
old-location: base\ivdsadvanceddisk.htm
old-project: VDS
ms.assetid: 6b5e1bff-e7e8-4403-99ff-6dc97d113f37
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsAdvancedDisk, IVdsAdvancedDisk interface [VDS], IVdsAdvancedDisk interface [VDS],described, base.ivdsadvanceddisk, vds/IVdsAdvancedDisk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsAdvancedDisk
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAdvancedDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates and deletes partitions, and modifies partition attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdvancedDisk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsAdvancedDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAdvancedDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92a79b87-7385-40d9-aa20-e4724b241e59">AssignDriveLetter</a>
</td>
<td align="left" width="63%">
Assigns a drive letter to an OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0345a4b1-bbe1-4e59-9a04-bb40ff6db954">ChangeAttributes</a>
</td>
<td align="left" width="63%">
Modifies partition attributes. For GPT disks, it applies to partition GPT attributes. For MBR disks, it applies to the boot indicator bit (active or not).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4052f294-d911-44c6-a57f-0a0a6f24df70">Clean</a>
</td>
<td align="left" width="63%">
Removes MBR or GPT information and uninitializes a basic or dynamic disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922669">CreatePartition</a>
</td>
<td align="left" width="63%">
Creates a partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1df6bf7e-0155-463c-85e2-c879557bc044">DeleteDriveLetter</a>
</td>
<td align="left" width="63%">
Deletes a drive letter from an OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b1a9d18-5f0b-4535-b0fb-6b1929099c1a">DeletePartition</a>
</td>
<td align="left" width="63%">
Deletes an existing partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b7015c2-a85d-4a56-8aec-208933640185">FormatPartition</a>
</td>
<td align="left" width="63%">
Formats an existing OEM, ESP or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de914162-3d55-4766-89d8-da2a531e9362">GetDriveLetter</a>
</td>
<td align="left" width="63%">
Retrieves the drive letter assigned to a OEM, ESP or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dc96e7b-34e5-4366-8804-d40f111d77c2">GetPartitionProperties</a>
</td>
<td align="left" width="63%">
Retrieves property information for a partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca02c5f8-11cd-4bdf-a376-3b146eb2aa70">QueryPartitions</a>
</td>
<td align="left" width="63%">
Retrieves information about all partitions on the current disk.

</td>
</tr>
</table> 


## -remarks




        The relationship between partitions and volumes is complex, and is best described in terms of the software provider (basic or dynamic) that manages the disk. Basic providers support the following three categories of partitions:

<ul>
<li>Partitions that are not volumes, because you can neither format them nor assign a drive letter to them. These partitions are MSR partitions, LDM Metadata partitions, and extended partitions. </li>
<li>Partitions associated with hidden volumes, which you can format and assign a drive letter to, but which host no user data. Instead, the system uses these partitions for booting, recovery, and so on. The partitions include OEM partitions, ESP partitions on GPT disks, and Unknown partitions. You cannot use the <a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a> or <a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a> interfaces to format these partitions. Instead, use the <b>IVdsAdvancedDisk</b> interface, which exposes the <a href="https://msdn.microsoft.com/92a79b87-7385-40d9-aa20-e4724b241e59">AssignDriveLetter</a>, <a href="https://msdn.microsoft.com/1df6bf7e-0155-463c-85e2-c879557bc044">DeleteDriveLetter</a>, and <a href="https://msdn.microsoft.com/9b7015c2-a85d-4a56-8aec-208933640185">FormatPartition</a> methods.

</li>
<li>Partitions that do not fall into the preceding two categories hold user data, files, and the installed operating system for the user. These partitions are always volumes; you can format them, assign  drive letters to them, and enumerate through them with the <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> and <a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a> functions.</li>
</ul>

In general, dynamic providers  do not map volumes to partitions. The exceptions are system volumes, boot volumes, and volumes for which the caller explicitly requests this mapping. 
Only the <a href="https://msdn.microsoft.com/6dc96e7b-34e5-4366-8804-d40f111d77c2">GetPartitionProperties</a>, <a href="https://msdn.microsoft.com/ca02c5f8-11cd-4bdf-a376-3b146eb2aa70">QueryPartitions</a>, and <a href="https://msdn.microsoft.com/4052f294-d911-44c6-a57f-0a0a6f24df70">Clean</a> methods are valid operations to be performed on dynamic disks. All other methods fail. Except for the <b>Clean</b> method, configuration-type operations are not valid on dynamic disks.




## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

