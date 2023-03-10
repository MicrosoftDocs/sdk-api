---
UID: NF:shimgdata.IShellImageData.GetResolution
title: IShellImageData::GetResolution (shimgdata.h)
description: Gets the resolution, in dots per inch (dpi), of the image.
helpviewer_keywords: ["GetResolution","GetResolution method [Windows Shell]","GetResolution method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetResolution method","IShellImageData.GetResolution","IShellImageData::GetResolution","_shell_IShellImageData_GetResolution","shell.IShellImageData_GetResolution","shimgdata/IShellImageData::GetResolution"]
old-location: shell\IShellImageData_GetResolution.htm
tech.root: shell
ms.assetid: 9e3c3e0f-010b-4d7d-a8fa-178a808687f8
ms.date: 12/05/2018
ms.keywords: GetResolution, GetResolution method [Windows Shell], GetResolution method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetResolution method, IShellImageData.GetResolution, IShellImageData::GetResolution, _shell_IShellImageData_GetResolution, shell.IShellImageData_GetResolution, shimgdata/IShellImageData::GetResolution
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
 - IShellImageData::GetResolution
 - shimgdata/IShellImageData::GetResolution
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
 - IShellImageData.GetResolution
---

# IShellImageData::GetResolution


## -description

Gets the resolution, in dots per inch (dpi), of the image.

## -parameters

### -param puResolutionX [out]

Type: <b>ULONG*</b>

A pointer to the horizontal resolution.

### -param puResolutionY [out]

Type: <b>ULONG*</b>

A pointer to the vertical resolution.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has not been decoded, the decode process failed, or the resolution cannot be retrieved. In the latter case, both <i>puResolutionX</i> and <i>puResolutionY</i> are set to 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Both <i>puResolutionX</i> and <i>puResolutionY</i> are <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If either <i>puResolutionX</i> or <i>puResolutionY</i> are <b>NULL</b>, the method returns only the value for the non-null parameter.

