---
UID: NF:shimgdata.IShellImageData.IsEditable
title: IShellImageData::IsEditable (shimgdata.h)
description: Determines whether the image can be edited.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","IsEditable method","IShellImageData.IsEditable","IShellImageData::IsEditable","IsEditable","IsEditable method [Windows Shell]","IsEditable method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_IsEditable","shell.IShellImageData_IsEditable","shimgdata/IShellImageData::IsEditable"]
old-location: shell\IShellImageData_IsEditable.htm
tech.root: shell
ms.assetid: 81dbb486-0b35-44ff-9aa2-2e449995591e
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],IsEditable method, IShellImageData.IsEditable, IShellImageData::IsEditable, IsEditable, IsEditable method [Windows Shell], IsEditable method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsEditable, shell.IShellImageData_IsEditable, shimgdata/IShellImageData::IsEditable
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::IsEditable
 - shimgdata/IShellImageData::IsEditable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.IsEditable
---

# IShellImageData::IsEditable


## -description

Determines whether the image can be edited.



## -returns

Type: <b>HRESULT</b>

Returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The image can be edited.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image cannot be edited, the image has not been decoded, or the decoding process failed.

</td>
</tr>
</table>

## -remarks

At this time, the criteria for determining whether the image can be edited is solely that it is a Tagged Image File Format (TIFF) image with the Exif IFD tag set.

