---
UID: NN:vds.IVdsAdvancedDisk
title: IVdsAdvancedDisk (vds.h)
description: Creates and deletes partitions, and modifies partition attributes.
helpviewer_keywords: ["IVdsAdvancedDisk","IVdsAdvancedDisk interface [VDS]","IVdsAdvancedDisk interface [VDS]","described","base.ivdsadvanceddisk","vds/IVdsAdvancedDisk"]
old-location: base\ivdsadvanceddisk.htm
tech.root: base
ms.assetid: 6b5e1bff-e7e8-4403-99ff-6dc97d113f37
ms.date: 12/05/2018
ms.keywords: IVdsAdvancedDisk, IVdsAdvancedDisk interface [VDS], IVdsAdvancedDisk interface [VDS],described, base.ivdsadvanceddisk, vds/IVdsAdvancedDisk
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAdvancedDisk
 - vds/IVdsAdvancedDisk
dev_langs:
 - c++
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
---

# IVdsAdvancedDisk interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates and deletes partitions, and modifies partition attributes.

## -inheritance

The <b>IVdsAdvancedDisk</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAdvancedDisk</b> also has these types of members:

## -remarks

The relationship between partitions and volumes is complex, and is best described in terms of the software provider (basic or dynamic) that manages the disk. Basic providers support the following three categories of partitions:

<ul>
<li>Partitions that are not volumes, because you can neither format them nor assign a drive letter to them. These partitions are MSR partitions, LDM Metadata partitions, and extended partitions. </li>
<li>Partitions associated with hidden volumes, which you can format and assign a drive letter to, but which host no user data. Instead, the system uses these partitions for booting, recovery, and so on. The partitions include OEM partitions, ESP partitions on GPT disks, and Unknown partitions. You cannot use the <a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a> or <a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a> interfaces to format these partitions. Instead, use the <b>IVdsAdvancedDisk</b> interface, which exposes the <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-assigndriveletter">AssignDriveLetter</a>, <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-deletedriveletter">DeleteDriveLetter</a>, and <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">FormatPartition</a> methods.

</li>
<li>Partitions that do not fall into the preceding two categories hold user data, files, and the installed operating system for the user. These partitions are always volumes; you can format them, assign  drive letters to them, and enumerate through them with the <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> functions.</li>
</ul>
In general, dynamic providers  do not map volumes to partitions. The exceptions are system volumes, boot volumes, and volumes for which the caller explicitly requests this mapping. 
Only the <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-getpartitionproperties">GetPartitionProperties</a>, <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-querypartitions">QueryPartitions</a>, and <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">Clean</a> methods are valid operations to be performed on dynamic disks. All other methods fail. Except for the <b>Clean</b> method, configuration-type operations are not valid on dynamic disks.

## -see-also

<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
