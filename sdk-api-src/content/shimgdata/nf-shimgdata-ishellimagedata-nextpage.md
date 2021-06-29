---
UID: NF:shimgdata.IShellImageData.NextPage
title: IShellImageData::NextPage (shimgdata.h)
description: Switches to the next page of a multipage image. Any associated animations are reset.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","NextPage method","IShellImageData.NextPage","IShellImageData::NextPage","NextPage","NextPage method [Windows Shell]","NextPage method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_NextPage","shell.IShellImageData_NextPage","shimgdata/IShellImageData::NextPage"]
old-location: shell\IShellImageData_NextPage.htm
tech.root: shell
ms.assetid: 19a2680a-f435-45c9-9573-e32f3cfdd090
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],NextPage method, IShellImageData.NextPage, IShellImageData::NextPage, NextPage, NextPage method [Windows Shell], NextPage method [Windows Shell],IShellImageData interface, _shell_IShellImageData_NextPage, shell.IShellImageData_NextPage, shimgdata/IShellImageData::NextPage
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
 - IShellImageData::NextPage
 - shimgdata/IShellImageData::NextPage
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
 - IShellImageData.NextPage
---

# IShellImageData::NextPage


## -description

Switches to the next page of a multipage image. Any associated animations are reset.



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
The current page cannot be retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ENUM_NOMORE</b></dt>
</dl>
</td>
<td width="60%">
No further pages are available, the image was not previously decoded, or the decode process failed.

</td>
</tr>
</table>

