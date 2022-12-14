---
UID: NF:shimgdata.IShellImageData.PrevPage
title: IShellImageData::PrevPage (shimgdata.h)
description: Switches to the previous page of a multipage image. Any associated animations are reset.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","PrevPage method","IShellImageData.PrevPage","IShellImageData::PrevPage","PrevPage","PrevPage method [Windows Shell]","PrevPage method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_PrevPage","shell.IShellImageData_PrevPage","shimgdata/IShellImageData::PrevPage"]
old-location: shell\IShellImageData_PrevPage.htm
tech.root: shell
ms.assetid: d3a4f07e-a1c0-4180-a02c-12eaebaaf1d2
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],PrevPage method, IShellImageData.PrevPage, IShellImageData::PrevPage, PrevPage, PrevPage method [Windows Shell], PrevPage method [Windows Shell],IShellImageData interface, _shell_IShellImageData_PrevPage, shell.IShellImageData_PrevPage, shimgdata/IShellImageData::PrevPage
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
 - IShellImageData::PrevPage
 - shimgdata/IShellImageData::PrevPage
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
 - IShellImageData.PrevPage
---

# IShellImageData::PrevPage


## -description

Switches to the previous page of a multipage image. Any associated animations are reset.



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
<dt><b>OLE_E_ENUM_NOMORE</b></dt>
</dl>
</td>
<td width="60%">
No previous pages are available, the image was not previously decoded, or the decode process failed.

</td>
</tr>
</table>

