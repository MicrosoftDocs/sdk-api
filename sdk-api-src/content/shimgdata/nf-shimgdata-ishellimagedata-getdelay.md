---
UID: NF:shimgdata.IShellImageData.GetDelay
title: IShellImageData::GetDelay (shimgdata.h)
description: Gets the delay value for the current frame of an animation.
helpviewer_keywords: ["GetDelay","GetDelay method [Windows Shell]","GetDelay method [Windows Shell]","IShellImageData interface","IShellImageData interface [Windows Shell]","GetDelay method","IShellImageData.GetDelay","IShellImageData::GetDelay","_shell_IShellImageData_GetDelay","shell.IShellImageData_GetDelay","shimgdata/IShellImageData::GetDelay"]
old-location: shell\IShellImageData_GetDelay.htm
tech.root: shell
ms.assetid: b5815771-7c96-4431-bc43-a5e620bd1d2f
ms.date: 12/05/2018
ms.keywords: GetDelay, GetDelay method [Windows Shell], GetDelay method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetDelay method, IShellImageData.GetDelay, IShellImageData::GetDelay, _shell_IShellImageData_GetDelay, shell.IShellImageData_GetDelay, shimgdata/IShellImageData::GetDelay
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
 - IShellImageData::GetDelay
 - shimgdata/IShellImageData::GetDelay
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
 - IShellImageData.GetDelay
---

# IShellImageData::GetDelay


## -description

Gets the delay value for the current frame of an animation.

## -parameters

### -param pdwDelay [out]

Type: <b>DWORD*</b>

A pointer to the delay value, in milliseconds. This value is valid only when the method returns S_OK.

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

Delay can vary from frame to frame in an animated image.

This method retrieves a minimum value of 100 milliseconds. Values less than that duration are also reported as 100 milliseconds.

