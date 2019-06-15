---
UID: NN:vds.IVdsAdvancedDisk
title: IVdsAdvancedDisk (vds.h)
author: windows-sdk-content
description: Creates and deletes partitions, and modifies partition attributes.
old-location: base\ivdsadvanceddisk.htm
tech.root: VDS
ms.assetid: 6b5e1bff-e7e8-4403-99ff-6dc97d113f37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsAdvancedDisk, IVdsAdvancedDisk interface [VDS], IVdsAdvancedDisk interface [VDS],described, base.ivdsadvanceddisk, vds/IVdsAdvancedDisk
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAdvancedDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdvancedDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates and deletes partitions, and modifies partition attributes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdvancedDisk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAdvancedDisk</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-assigndriveletter">AssignDriveLetter</a>
</td>
<td align="left" width="63%">
Assigns a drive letter to an OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-changeattributes">ChangeAttributes</a>
</td>
<td align="left" width="63%">
Modifies partition attributes. For GPT disks, it applies to partition GPT attributes. For MBR disks, it applies to the boot indicator bit (active or not).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">Clean</a>
</td>
<td align="left" width="63%">
Removes MBR or GPT information and uninitializes a basic or dynamic disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">CreatePartition</a>
</td>
<td align="left" width="63%">
Creates a partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-deletedriveletter">DeleteDriveLetter</a>
</td>
<td align="left" width="63%">
Deletes a drive letter from an OEM, ESP, or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-deletepartition">DeletePartition</a>
</td>
<td align="left" width="63%">
Deletes an existing partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">FormatPartition</a>
</td>
<td align="left" width="63%">
Formats an existing OEM, ESP or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getdriveletter">GetDriveLetter</a>
</td>
<td align="left" width="63%">
Retrieves the drive letter assigned to a OEM, ESP or unknown partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getpartitionproperties">GetPartitionProperties</a>
</td>
<td align="left" width="63%">
Retrieves property information for a partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-querypartitions">QueryPartitions</a>
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
<li>Partitions associated with hidden volumes, which you can format and assign a drive letter to, but which host no user data. Instead, the system uses these partitions for booting, recovery, and so on. The partitions include OEM partitions, ESP partitions on GPT disks, and Unknown partitions. You cannot use the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a> or <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a> interfaces to format these partitions. Instead, use the <b>IVdsAdvancedDisk</b> interface, which exposes the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-assigndriveletter">AssignDriveLetter</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-deletedriveletter">DeleteDriveLetter</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">FormatPartition</a> methods.

</li>
<li>Partitions that do not fall into the preceding two categories hold user data, files, and the installed operating system for the user. These partitions are always volumes; you can format them, assign  drive letters to them, and enumerate through them with the <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> functions.</li>
</ul>
In general, dynamic providers  do not map volumes to partitions. The exceptions are system volumes, boot volumes, and volumes for which the caller explicitly requests this mapping. 
Only the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getpartitionproperties">GetPartitionProperties</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-querypartitions">QueryPartitions</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">Clean</a> methods are valid operations to be performed on dynamic disks. All other methods fail. Except for the <b>Clean</b> method, configuration-type operations are not valid on dynamic disks.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

