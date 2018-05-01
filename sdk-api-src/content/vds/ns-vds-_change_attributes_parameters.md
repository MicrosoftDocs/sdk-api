---
UID: NS:vds._CHANGE_ATTRIBUTES_PARAMETERS
title: "_CHANGE_ATTRIBUTES_PARAMETERS"
author: windows-driver-content
description: Defines the partition parameters of a partition style.
old-location: base\change_attributes_parameters.htm
old-project: VDS
ms.assetid: 6ff3ea68-70dd-4ef1-9c31-1f8c1fcf5fca
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CHANGE_ATTRIBUTES_PARAMETERS, CHANGE_ATTRIBUTES_PARAMETERS structure [VDS], GPT_ATTRIBUTE_PLATFORM_REQUIRED, GPT_BASIC_DATA_ATTRIBUTE_HIDDEN, GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER, GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY, GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY, _CHANGE_ATTRIBUTES_PARAMETERS, base.change_attributes_parameters, vds/CHANGE_ATTRIBUTES_PARAMETERS
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CHANGE_ATTRIBUTES_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	CHANGE_ATTRIBUTES_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _CHANGE_ATTRIBUTES_PARAMETERS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the partition parameters of a partition style.


## -struct-fields




### -field style

Determines the partition parameters. Supported values are <b>VDS_PST_MBR</b> or 
      <b>VDS_PST_GPT</b>.


### -field MbrPartInfo

Used if <b>style</b> is <b>VDS_PST_MBR</b>. Parameters for a Master 
       Boot Record (MBR) disk.


### -field MbrPartInfo.bootIndicator

If <b>TRUE</b>, the partition is active and can be booted; otherwise the partition 
        cannot be used to boot the system.


### -field GptPartInfo

Used if <b>style</b> is <b>VDS_PST_GPT</b>. Parameters for a GUID 
       Partition Table (GPT) disk.


### -field GptPartInfo.attributes


Attributes of the partition. This can be one or more of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GPT_ATTRIBUTE_PLATFORM_REQUIRED"></a><a id="gpt_attribute_platform_required"></a><dl>
<dt><b>GPT_ATTRIBUTE_PLATFORM_REQUIRED</b></dt>
<dt>0x0000000000000001</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is required by a computer to function properly. 

For example, 
          this attribute must be set for OEM partitions. Note that if this attribute is set, you can use the DiskPart.exe utility to perform partition operations such as deleting the partition. However, because the partition is not a volume, you cannot use the DiskPart.exe utility to perform volume operations on the partition.

This attribute can be set for basic and dynamic disks. If it is set for a partition on a basic disk and the disk is converted to a dynamic disk, the partition remains a basic partition, even though the rest of the disk is a dynamic disk. This is because the partition is considered to be an OEM partition on a GPT disk.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER"></a><a id="gpt_basic_data_attribute_no_drive_letter"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER</b></dt>
<dt>0x8000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition does not receive a drive letter by default when the disk is moved to another computer or the disk is seen for the first time by a computer. 

This attribute is 
          useful in SAN environments.

Despite its name, this attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_HIDDEN"></a><a id="gpt_basic_data_attribute_hidden"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_HIDDEN</b></dt>
<dt>0x4000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is not detected by the Mount Manager. 

As a result, the partition does not receive a drive letter, 
          does not receive a volume GUID path, does not host mounted folders (also called volume mount points), and is not enumerated by calls to 
          <a href="https://msdn.microsoft.com/3eaf9903-ae20-47e7-b32c-943bf60e7bbd">FindFirstVolume</a> and 
          <a href="https://msdn.microsoft.com/6ab4467a-f84a-403e-9327-b523ceead19f">FindNextVolume</a>. This ensures that applications 
          such as Disk Defragmenter do not access the partition. The Volume Shadow Copy Service (VSS) uses this attribute.

Despite its name, this attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY"></a><a id="gpt_basic_data_attribute_shadow_copy"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY</b></dt>
<dt>0x2000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is a shadow copy of another partition. 

This attribute is used by the Volume Shadow Copy service (VSS). This attribute is an indication for file system filter driver-based software (such as 
          antivirus programs) to avoid attaching to the volume.

An application can use the attribute to differentiate 
          a shadow copy volume from a production volume. An application that performs a fast recovery, for example, will break a shadow copy LUN by clearing the read-only and hidden attributes and this attribute. This attribute is set when the shadow copy is created and cleared when the shadow copy is broken.

Despite its name, this attribute can be set for basic and dynamic disks.

<b>Windows Server 2003:  </b>This attribute is not supported before Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY"></a><a id="gpt_basic_data_attribute_read_only"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x1000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is read-only. 

All requests to write to the partition will fail. 
          <a href="https://msdn.microsoft.com/library/windows/hardware/ff560384">IOCTL_DISK_IS_WRITABLE</a> will fail with the 
          ERROR_WRITE_PROTECT Win32 error code, which causes the file system to mount as read-only, if a file system is present.

VSS uses this attribute.

Do not set this attribute for dynamic disks. Setting it can cause I/O errors and prevent the file system from mounting properly.

</td>
</tr>
</table>
 


## -remarks



The 
    <a href="https://msdn.microsoft.com/0345a4b1-bbe1-4e59-9a04-bb40ff6db954">IVdsAdvancedDisk::ChangeAttributes</a> 
    method takes this structure as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/0345a4b1-bbe1-4e59-9a04-bb40ff6db954">IVdsAdvancedDisk::ChangeAttributes</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>
 

 

