---
UID: NF:shimgdata.IShellImageData.IsAnimated
title: IShellImageData::IsAnimated (shimgdata.h)
description: Determines whether the image is animated.
old-location: shell\IShellImageData_IsAnimated.htm
tech.root: shell
ms.assetid: b5b36862-5beb-4702-a5b3-feb70dc5e1ef
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],IsAnimated method, IShellImageData.IsAnimated, IShellImageData::IsAnimated, IsAnimated, IsAnimated method [Windows Shell], IsAnimated method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsAnimated, shell.IShellImageData_IsAnimated, shimgdata/IShellImageData::IsAnimated
f1_keywords:
- shimgdata/IShellImageData.IsAnimated
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IShellImageData.IsAnimated
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellImageData::IsAnimated


## -description


Determines whether the image is animated.


## -parameters






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
The image is animated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The image is not animated, has not been decoded, or the decoding process failed.

</td>
</tr>
</table>
 



