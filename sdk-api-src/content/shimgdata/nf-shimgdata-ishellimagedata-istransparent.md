---
UID: NF:shimgdata.IShellImageData.IsTransparent
title: IShellImageData::IsTransparent (shimgdata.h)
description: Determines whether the image is transparent.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","IsTransparent method","IShellImageData.IsTransparent","IShellImageData::IsTransparent","IsTransparent","IsTransparent method [Windows Shell]","IsTransparent method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_IsTransparent","shell.IShellImageData_IsTransparent","shimgdata/IShellImageData::IsTransparent"]
old-location: shell\IShellImageData_IsTransparent.htm
tech.root: shell
ms.assetid: 613d2c01-47d5-41c3-8dba-5b1e1feabdf3
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],IsTransparent method, IShellImageData.IsTransparent, IShellImageData::IsTransparent, IsTransparent, IsTransparent method [Windows Shell], IsTransparent method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsTransparent, shell.IShellImageData_IsTransparent, shimgdata/IShellImageData::IsTransparent
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
 - IShellImageData::IsTransparent
 - shimgdata/IShellImageData::IsTransparent
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
 - IShellImageData.IsTransparent
---

# IShellImageData::IsTransparent


## -description

Determines whether the image is transparent.



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
The image has transparency.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image does not have transparency.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has not been decoded.

</td>
</tr>
</table>

## -remarks

If an image supports transparency but does not use it, the method returns S_FALSE.

