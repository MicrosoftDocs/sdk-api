---
UID: NF:shimgdata.IShellImageData.NextFrame
title: IShellImageData::NextFrame (shimgdata.h)
description: Switches to the next frame of an animated image.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","NextFrame method","IShellImageData.NextFrame","IShellImageData::NextFrame","NextFrame","NextFrame method [Windows Shell]","NextFrame method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_NextFrame","shell.IShellImageData_NextFrame","shimgdata/IShellImageData::NextFrame"]
old-location: shell\IShellImageData_NextFrame.htm
tech.root: shell
ms.assetid: b797539e-7766-4da7-864f-401c7c2ff082
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],NextFrame method, IShellImageData.NextFrame, IShellImageData::NextFrame, NextFrame, NextFrame method [Windows Shell], NextFrame method [Windows Shell],IShellImageData interface, _shell_IShellImageData_NextFrame, shell.IShellImageData_NextFrame, shimgdata/IShellImageData::NextFrame
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
 - IShellImageData::NextFrame
 - shimgdata/IShellImageData::NextFrame
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
 - IShellImageData.NextFrame
---

# IShellImageData::NextFrame


## -description

Switches to the next frame of an animated image.



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
The current frame cannot be retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image is not animated, the image has not yet been decoded, or a limit on the number of times to loop the animation has been reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The next frame is not yet available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOMOREDATA</b></dt>
</dl>
</td>
<td width="60%">
No further data is available.

</td>
</tr>
</table>

