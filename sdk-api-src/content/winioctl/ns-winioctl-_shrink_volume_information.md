---
UID: NS:winioctl._SHRINK_VOLUME_INFORMATION
title: "_SHRINK_VOLUME_INFORMATION"
author: windows-sdk-content
description: Specifies the volume shrink operation to perform.
old-location: fs\shrink_volume_information.htm
old-project: fileio
ms.assetid: 91e2c4a1-7b95-49d9-9f28-c3ce4355f1ea
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSHRINK_VOLUME_INFORMATION, PSHRINK_VOLUME_INFORMATION, PSHRINK_VOLUME_INFORMATION structure pointer [Files], SHRINK_VOLUME_INFORMATION, SHRINK_VOLUME_INFORMATION structure [Files], ShrinkAbort, ShrinkCommit, ShrinkPrepare, _SHRINK_VOLUME_INFORMATION, fs.shrink_volume_information, winioctl/PSHRINK_VOLUME_INFORMATION, winioctl/SHRINK_VOLUME_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SHRINK_VOLUME_INFORMATION, *PSHRINK_VOLUME_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - SHRINK_VOLUME_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _SHRINK_VOLUME_INFORMATION structure


## -description


Specifies the volume shrink operation to perform.


## -struct-fields




### -field ShrinkRequestType

Indicates the operation to perform. The valid values are as follows. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ShrinkPrepare"></a><a id="shrinkprepare"></a><a id="SHRINKPREPARE"></a><dl>
<dt><b>ShrinkPrepare</b></dt>
</dl>
</td>
<td width="60%">
Volume should perform any steps necessary to prepare for a shrink operation.

</td>
</tr>
<tr>
<td width="40%"><a id="ShrinkCommit"></a><a id="shrinkcommit"></a><a id="SHRINKCOMMIT"></a><dl>
<dt><b>ShrinkCommit</b></dt>
</dl>
</td>
<td width="60%">
Volume should commit the shrink operation changes.

</td>
</tr>
<tr>
<td width="40%"><a id="ShrinkAbort"></a><a id="shrinkabort"></a><a id="SHRINKABORT"></a><dl>
<dt><b>ShrinkAbort</b></dt>
</dl>
</td>
<td width="60%">
Volume should terminate the shrink operation.

</td>
</tr>
</table>
 


### -field Flags

This member must be zero.


### -field NewNumberOfSectors

The number of sectors that should be in the shrunken volume. Used only when the <b>ShrinkRequestType</b> member is <b>ShrinkPrepare</b>, otherwise this member should be initialized to zero.


## -see-also




<a href="https://msdn.microsoft.com/cf545417-f933-4054-bed4-e6adbf822f9c">FSCTL_SHRINK_VOLUME</a>
 

 

