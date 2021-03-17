---
UID: NF:shimgdata.IShellImageData.SelectPage
title: IShellImageData::SelectPage (shimgdata.h)
description: Selects a specified page in a multipage image.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","SelectPage method","IShellImageData.SelectPage","IShellImageData::SelectPage","SelectPage","SelectPage method [Windows Shell]","SelectPage method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_SelectPage","shell.IShellImageData_SelectPage","shimgdata/IShellImageData::SelectPage"]
old-location: shell\IShellImageData_SelectPage.htm
tech.root: shell
ms.assetid: bc852087-59f7-4c84-861a-e270a6ecf840
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],SelectPage method, IShellImageData.SelectPage, IShellImageData::SelectPage, SelectPage, SelectPage method [Windows Shell], SelectPage method [Windows Shell],IShellImageData interface, _shell_IShellImageData_SelectPage, shell.IShellImageData_SelectPage, shimgdata/IShellImageData::SelectPage
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
 - IShellImageData::SelectPage
 - shimgdata/IShellImageData::SelectPage
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
 - IShellImageData.SelectPage
---

# IShellImageData::SelectPage


## -description

Selects a specified page in a multipage image.

## -parameters

### -param iPage [in]

Type: <b>ULONG</b>

The page number of the page to select.

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
The current page cannot be retrieved, the image has not been decoded, or the decoding process failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ENUM_NOMORE</b></dt>
</dl>
</td>
<td width="60%">
The specified page number does not exist.

</td>
</tr>
</table>

