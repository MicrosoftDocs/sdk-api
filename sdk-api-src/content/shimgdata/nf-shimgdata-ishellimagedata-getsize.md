---
UID: NF:shimgdata.IShellImageData.GetSize
title: IShellImageData::GetSize (shimgdata.h)
description: Gets the dimensions of the image file.
helpviewer_keywords: ["GetSize","GetSize method [Windows Shell]","GetSize method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetSize method","IShellImageData.GetSize","IShellImageData::GetSize","_shell_IShellImageData_GetSize","shell.IShellImageData_GetSize","shimgdata/IShellImageData::GetSize"]
old-location: shell\IShellImageData_GetSize.htm
tech.root: shell
ms.assetid: 50294d95-801d-4cd6-94ae-8b48c68af50f
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Windows Shell], GetSize method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetSize method, IShellImageData.GetSize, IShellImageData::GetSize, _shell_IShellImageData_GetSize, shell.IShellImageData_GetSize, shimgdata/IShellImageData::GetSize
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
 - IShellImageData::GetSize
 - shimgdata/IShellImageData::GetSize
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
 - IShellImageData.GetSize
---

# IShellImageData::GetSize


## -description

Gets the dimensions of the image file.

## -parameters

### -param pSize [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure containing the size of the image. This value is valid only when the method returns <b>S_OK</b>.

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