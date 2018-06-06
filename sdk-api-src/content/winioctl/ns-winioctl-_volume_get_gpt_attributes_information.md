---
UID: NS:winioctl._VOLUME_GET_GPT_ATTRIBUTES_INFORMATION
title: "_VOLUME_GET_GPT_ATTRIBUTES_INFORMATION"
author: windows-sdk-content
description: Contains volume attributes retrieved with the IOCTL_VOLUME_GET_GPT_ATTRIBUTES control code.
old-location: fs\volume_get_gpt_attributes_information.htm
old-project: FileIO
ms.assetid: d67590a9-9182-406f-8d15-8d40172cf5e5
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION, GPT_BASIC_DATA_ATTRIBUTE_HIDDEN, GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER, GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY, GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY, PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION, PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION structure pointer [Files], VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, VOLUME_GET_GPT_ATTRIBUTES_INFORMATION structure [Files], _VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, fs.volume_get_gpt_attributes_information, winioctl/PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION, winioctl/VOLUME_GET_GPT_ATTRIBUTES_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - VOLUME_GET_GPT_ATTRIBUTES_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _VOLUME_GET_GPT_ATTRIBUTES_INFORMATION structure


## -description


Contains volume attributes retrieved with the <a href="https://msdn.microsoft.com/3e58e0d6-215a-47f3-b1bf-e8d53c224b68">IOCTL_VOLUME_GET_GPT_ATTRIBUTES</a> control code.


## -struct-fields




### -field GptAttributes

Specifies all of the attributes
    associated with a volume.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY"></a><a id="gpt_basic_data_attribute_read_only"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x1000000000000000</dt>
</dl>
</td>
<td width="60%">
The volume is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY"></a><a id="gpt_basic_data_attribute_shadow_copy"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY</b></dt>
<dt>0x2000000000000000</dt>
</dl>
</td>
<td width="60%">
The volume is a shadow copy of another volume. For more information, see <a href="https://msdn.microsoft.com/263b0200-4869-4fb0-ad50-240166d2d32f">Volume Shadow Copy Service Overview</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_HIDDEN"></a><a id="gpt_basic_data_attribute_hidden"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_HIDDEN</b></dt>
<dt>0x4000000000000000</dt>
</dl>
</td>
<td width="60%">
The volume is hidden.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER"></a><a id="gpt_basic_data_attribute_no_drive_letter"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER</b></dt>
<dt>0x8000000000000000</dt>
</dl>
</td>
<td width="60%">
The volume is not assigned a default drive letter.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/3e58e0d6-215a-47f3-b1bf-e8d53c224b68">IOCTL_VOLUME_GET_GPT_ATTRIBUTES</a>
 

 

