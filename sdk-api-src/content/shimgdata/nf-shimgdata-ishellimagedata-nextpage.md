---
UID: NF:shimgdata.IShellImageData.NextPage
title: IShellImageData::NextPage
author: windows-sdk-content
description: Switches to the next page of a multipage image. Any associated animations are reset.
old-location: shell\IShellImageData_NextPage.htm
tech.root: Shell
ms.assetid: 19a2680a-f435-45c9-9573-e32f3cfdd090
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IShellImageData interface [Windows Shell],NextPage method, IShellImageData.NextPage, IShellImageData::NextPage, NextPage, NextPage method [Windows Shell], NextPage method [Windows Shell],IShellImageData interface, _shell_IShellImageData_NextPage, shell.IShellImageData_NextPage, shimgdata/IShellImageData::NextPage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IShellImageData.NextPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::NextPage


## -description


Switches to the next page of a multipage image. Any associated animations are reset.


## -parameters






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
 



