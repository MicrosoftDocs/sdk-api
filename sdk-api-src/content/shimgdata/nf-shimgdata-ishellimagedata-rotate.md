---
UID: NF:shimgdata.IShellImageData.Rotate
title: IShellImageData::Rotate (shimgdata.h)
description: Rotates an image in increments of 90 degrees.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","Rotate method","IShellImageData.Rotate","IShellImageData::Rotate","Rotate","Rotate method [Windows Shell]","Rotate method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_Rotate","shell.IShellImageData_Rotate","shimgdata/IShellImageData::Rotate"]
old-location: shell\IShellImageData_Rotate.htm
tech.root: shell
ms.assetid: 42fd8596-e130-4029-bf3c-67199e8dd804
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],Rotate method, IShellImageData.Rotate, IShellImageData::Rotate, Rotate, Rotate method [Windows Shell], Rotate method [Windows Shell],IShellImageData interface, _shell_IShellImageData_Rotate, shell.IShellImageData_Rotate, shimgdata/IShellImageData::Rotate
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
 - IShellImageData::Rotate
 - shimgdata/IShellImageData::Rotate
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
 - IShellImageData.Rotate
---

# IShellImageData::Rotate


## -description

Rotates an image in increments of 90 degrees.

## -parameters

### -param dwAngle [in]

Type: <b>DWORD</b>

The angle of rotation. Only angles of 0, 90, 180, and 270 are recognized.

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
The image has not been decoded or the decoding process failed. This value is also returned when certain internal calls to GDI+ methods fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTVALIDFORANIMATEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image is an animated image and cannot be rotated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwAngle</i> parameter is a value other than 0, 90, 180, or 270.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwAngle</i> parameter is 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough resources are available for the method to create an internal working copy of the image.

</td>
</tr>
</table>

