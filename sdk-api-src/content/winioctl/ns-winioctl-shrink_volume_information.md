---
UID: NS:winioctl._SHRINK_VOLUME_INFORMATION
title: SHRINK_VOLUME_INFORMATION
description: Specifies the volume shrink operation to perform.
helpviewer_keywords: ["*PSHRINK_VOLUME_INFORMATION","PSHRINK_VOLUME_INFORMATION","PSHRINK_VOLUME_INFORMATION structure pointer [Files]","SHRINK_VOLUME_INFORMATION","SHRINK_VOLUME_INFORMATION structure [Files]","ShrinkAbort","ShrinkCommit","ShrinkPrepare","fs.shrink_volume_information","winioctl/PSHRINK_VOLUME_INFORMATION","winioctl/SHRINK_VOLUME_INFORMATION"]
old-location: fs\shrink_volume_information.htm
tech.root: fs
ms.assetid: 91e2c4a1-7b95-49d9-9f28-c3ce4355f1ea
ms.date: 12/05/2018
ms.keywords: '*PSHRINK_VOLUME_INFORMATION, PSHRINK_VOLUME_INFORMATION, PSHRINK_VOLUME_INFORMATION structure pointer [Files], SHRINK_VOLUME_INFORMATION, SHRINK_VOLUME_INFORMATION structure [Files], ShrinkAbort, ShrinkCommit, ShrinkPrepare, fs.shrink_volume_information, winioctl/PSHRINK_VOLUME_INFORMATION, winioctl/SHRINK_VOLUME_INFORMATION'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHRINK_VOLUME_INFORMATION, *PSHRINK_VOLUME_INFORMATION
req.redist: 
f1_keywords:
 - _SHRINK_VOLUME_INFORMATION
 - winioctl/_SHRINK_VOLUME_INFORMATION
 - PSHRINK_VOLUME_INFORMATION
 - winioctl/PSHRINK_VOLUME_INFORMATION
 - SHRINK_VOLUME_INFORMATION
 - winioctl/SHRINK_VOLUME_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - SHRINK_VOLUME_INFORMATION
---

# SHRINK_VOLUME_INFORMATION structure


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

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_shrink_volume">FSCTL_SHRINK_VOLUME</a>