---
UID: NF:shimgdata.IShellImageData.GetPageCount
title: IShellImageData::GetPageCount (shimgdata.h)
description: Gets the number of pages in a multipage image.
helpviewer_keywords: ["GetPageCount","GetPageCount method [Windows Shell]","GetPageCount method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetPageCount method","IShellImageData.GetPageCount","IShellImageData::GetPageCount","_shell_IShellImageData_GetPageCount","shell.IShellImageData_GetPageCount","shimgdata/IShellImageData::GetPageCount"]
old-location: shell\IShellImageData_GetPageCount.htm
tech.root: shell
ms.assetid: 5967a167-2cd5-4662-b624-e136c0092118
ms.date: 12/05/2018
ms.keywords: GetPageCount, GetPageCount method [Windows Shell], GetPageCount method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetPageCount method, IShellImageData.GetPageCount, IShellImageData::GetPageCount, _shell_IShellImageData_GetPageCount, shell.IShellImageData_GetPageCount, shimgdata/IShellImageData::GetPageCount
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
 - IShellImageData::GetPageCount
 - shimgdata/IShellImageData::GetPageCount
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
 - IShellImageData.GetPageCount
---

# IShellImageData::GetPageCount


## -description

Gets the number of pages in a multipage image.

## -parameters

### -param pcPages [out]

Type: <b>ULONG*</b>

A pointer to the page count. This value is valid only when the method returns S_OK.

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
The image has not been decoded or the decoding process failed.

</td>
</tr>
</table>

## -remarks

If the image is not a multipage image, such as a .jpg file, the method returns S_OK with a page count of 1.

