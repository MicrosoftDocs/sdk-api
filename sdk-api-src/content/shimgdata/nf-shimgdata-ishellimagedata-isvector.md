---
UID: NF:shimgdata.IShellImageData.IsVector
title: IShellImageData::IsVector
author: windows-sdk-content
description: Determines whether the image is a vector image.
old-location: shell\IShellImageData_IsVector.htm
old-project: shell
ms.assetid: a4099bc4-c831-4a4e-a3f6-932570dc8029
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IShellImageData interface [Windows Shell],IsVector method, IShellImageData.IsVector, IShellImageData::IsVector, IsVector, IsVector method [Windows Shell], IsVector method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsVector, shell.IShellImageData_IsVector, shimgdata/IShellImageData::IsVector
ms.prod: windows
ms.technology: windows-sdk
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
 - IShellImageData.IsVector
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::IsVector


## -description


Determines whether the image is a vector image.


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
The image is a vector image, supporting the GDI+ flag <a href="https://www.bing.com/search?q=ImageFlagsScalable">ImageFlagsScalable</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image has not been decoded, the image is empty, or the file is not an image.

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
 



