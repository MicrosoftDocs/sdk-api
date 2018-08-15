---
UID: NF:shimgdata.IShellImageData.GetPageCount
title: IShellImageData::GetPageCount
author: windows-sdk-content
description: Gets the number of pages in a multipage image.
old-location: shell\IShellImageData_GetPageCount.htm
old-project: shell
ms.assetid: 5967a167-2cd5-4662-b624-e136c0092118
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPageCount, GetPageCount method [Windows Shell], GetPageCount method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetPageCount method, IShellImageData.GetPageCount, IShellImageData::GetPageCount, _shell_IShellImageData_GetPageCount, shell.IShellImageData_GetPageCount, shimgdata/IShellImageData::GetPageCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shimgdata.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SHELL_UI_COMPONENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.GetPageCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
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



