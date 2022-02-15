---
UID: NF:shimgdata.IShellImageData.IsVector
title: IShellImageData::IsVector (shimgdata.h)
description: Determines whether the image is a vector image.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","IsVector method","IShellImageData.IsVector","IShellImageData::IsVector","IsVector","IsVector method [Windows Shell]","IsVector method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_IsVector","shell.IShellImageData_IsVector","shimgdata/IShellImageData::IsVector"]
old-location: shell\IShellImageData_IsVector.htm
tech.root: shell
ms.assetid: a4099bc4-c831-4a4e-a3f6-932570dc8029
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],IsVector method, IShellImageData.IsVector, IShellImageData::IsVector, IsVector, IsVector method [Windows Shell], IsVector method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsVector, shell.IShellImageData_IsVector, shimgdata/IShellImageData::IsVector
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
 - IShellImageData::IsVector
 - shimgdata/IShellImageData::IsVector
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
 - IShellImageData.IsVector
---

# IShellImageData::IsVector


## -description

Determines whether the image is a vector image.



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
The image is a vector image, supporting the GDI+ flag <a href="/windows/desktop/api/gdiplusimaging/ne-gdiplusimaging-imageflags">ImageFlagsScalable</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has not been decoded, the image is empty, or the file is not an image.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
All other cases.

</td>
</tr>
</table>
