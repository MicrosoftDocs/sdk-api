---
UID: NF:shimgdata.IShellImageData.GetEncoderParams
title: IShellImageData::GetEncoderParams
author: windows-sdk-content
description: Gets the current set of encoder parameters.
old-location: shell\IShellImageData_GetEncoderParams.htm
tech.root: shell
ms.assetid: 9b664d0f-7bb7-4cdd-8c0c-2ca80faaa764
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetEncoderParams, GetEncoderParams method [Windows Shell], GetEncoderParams method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetEncoderParams method, IShellImageData.GetEncoderParams, IShellImageData::GetEncoderParams, _shell_IShellImageData_GetEncoderParams, shell.IShellImageData_GetEncoderParams, shimgdata/IShellImageData::GetEncoderParams
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
 - IShellImageData.GetEncoderParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::GetEncoderParams


## -description


Gets the current set of encoder parameters.


## -parameters




### -param pguidFmt [in]

Type: <b>GUID*</b>

A pointer to a GUID that specifies the encoder. This must be an encoder supported by GDI+. If this parameter is <b>NULL</b>, an unhandled exception results.


### -param ppEncParams [out]

Type: <b>EncoderParameters**</b>

The address of a pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a> objects.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

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
Several circumstances can generate this return value.
                        

<ul>
<li>The image was not decoded or the decoding process failed.</li>
<li><i>pguidFmt</i> refers to a format not supported by GDI+.</li>
<li>An internal call failed.</li>
</ul>
</td>
</tr>
</table>
 



