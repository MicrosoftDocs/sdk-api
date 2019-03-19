---
UID: NF:shimgdata.IShellImageData.IsMultipage
title: IShellImageData::IsMultipage (shimgdata.h)
author: windows-sdk-content
description: Determines whether the image is a multipage Tagged Image File Format (TIFF) image.
old-location: shell\IShellImageData_IsMultipage.htm
tech.root: shell
ms.assetid: a9c86f0e-5237-432c-a2bb-4054a23d707e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellImageData interface [Windows Shell],IsMultipage method, IShellImageData.IsMultipage, IShellImageData::IsMultipage, IsMultipage, IsMultipage method [Windows Shell], IsMultipage method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsMultipage, shell.IShellImageData_IsMultipage, shimgdata/IShellImageData::IsMultipage
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
 - IShellImageData.IsMultipage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::IsMultipage


## -description


Determines whether the image is a multipage Tagged Image File Format (TIFF) image.


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
The image contains more than one page.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has only one page, the image has not been decoded, or the decoding process failed.

</td>
</tr>
</table>
 



