---
UID: NF:shimgdata.IShellImageData.GetPixelFormat
title: IShellImageData::GetPixelFormat (shimgdata.h)
description: Gets the pixel format of the image.
helpviewer_keywords: ["GetPixelFormat","GetPixelFormat method [Windows Shell]","GetPixelFormat method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetPixelFormat method","IShellImageData.GetPixelFormat","IShellImageData::GetPixelFormat","_shell_IShellImageData_GetPixelFormat","shell.IShellImageData_GetPixelFormat","shimgdata/IShellImageData::GetPixelFormat"]
old-location: shell\IShellImageData_GetPixelFormat.htm
tech.root: shell
ms.assetid: 43520cdd-66f1-4c75-bcec-7631de4f96c3
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [Windows Shell], GetPixelFormat method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetPixelFormat method, IShellImageData.GetPixelFormat, IShellImageData::GetPixelFormat, _shell_IShellImageData_GetPixelFormat, shell.IShellImageData_GetPixelFormat, shimgdata/IShellImageData::GetPixelFormat
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
 - IShellImageData::GetPixelFormat
 - shimgdata/IShellImageData::GetPixelFormat
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
 - IShellImageData.GetPixelFormat
---

# IShellImageData::GetPixelFormat


## -description

Gets the pixel format of the image.

## -parameters

### -param pFormat [out]

Type: <b>PixelFormat*</b>

A pointer to a value of type <a href="/windows/desktop/gdiplus/-gdiplus-constant-image-pixel-format-constants">PixelFormat</a> indicating the pixel format.  This value is valid only when the method returns <b>S_OK</b>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

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
The image has not been decoded or the decoding process failed.

</td>
</tr>
</table>

## -remarks

Values that identify various pixel formats are defined in Gdipluspixelformats.h.