---
UID: NF:shimgdata.IShellImageData.IsPrintable
title: IShellImageData::IsPrintable
author: windows-sdk-content
description: Determines whether the image can be printed.
old-location: shell\IShellImageData_IsPrintable.htm
old-project: shell
ms.assetid: 5c50e919-cb5b-4332-bc17-ad24f31cf680
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellImageData interface [Windows Shell],IsPrintable method, IShellImageData.IsPrintable, IShellImageData::IsPrintable, IsPrintable, IsPrintable method [Windows Shell], IsPrintable method [Windows Shell],IShellImageData interface, _shell_IShellImageData_IsPrintable, shell.IShellImageData_IsPrintable, shimgdata/IShellImageData::IsPrintable
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
 - IShellImageData.IsPrintable
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::IsPrintable


## -description


Determines whether the image can be printed.


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
The image has not been decoded.

</td>
</tr>
</table>
 



