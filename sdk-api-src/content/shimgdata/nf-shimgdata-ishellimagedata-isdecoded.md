---
UID: NF:shimgdata.IShellImageData.IsDecoded
title: IShellImageData::IsDecoded (shimgdata.h)
description: Determines whether the image has been decoded by calling IShellImageData::Decode. Many operations return a failure code if the image is not first decoded.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","IsDecoded method","IShellImageData.IsDecoded","IShellImageData::IsDecoded","IsDecoded","IsDecoded method [Windows Shell]","IsDecoded method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_IsDecoded","shell.IShellImageData_IsDecoded","shimgdata/IShellImageData::IsDecoded"]
old-location: shell\IShellImageData_IsDecoded.htm
tech.root: shell
ms.assetid: f02dbf35-4dc7-4750-978d-b703338514df
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],IsDecoded method, IShellImageData.IsDecoded, IShellImageData::IsDecoded, IsDecoded, IsDecoded method [Windows Shell], IsDecoded method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsDecoded, shell.IShellImageData_IsDecoded, shimgdata/IShellImageData::IsDecoded
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
 - IShellImageData::IsDecoded
 - shimgdata/IShellImageData::IsDecoded
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
 - IShellImageData.IsDecoded
---

# IShellImageData::IsDecoded


## -description

Determines whether the image has been decoded by calling <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">IShellImageData::Decode</a>. Many operations return a failure code if the image is not first decoded.



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

<a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-decode">IShellImageData::Decode</a> was called on the image and was successful.

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
