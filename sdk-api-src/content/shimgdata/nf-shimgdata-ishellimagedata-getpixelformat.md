---
UID: NF:shimgdata.IShellImageData.GetPixelFormat
title: IShellImageData::GetPixelFormat
author: windows-driver-content
description: Gets the pixel format of the image.
old-location: shell\IShellImageData_GetPixelFormat.htm
old-project: shell
ms.assetid: 43520cdd-66f1-4c75-bcec-7631de4f96c3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [Windows Shell], GetPixelFormat method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],GetPixelFormat method, IShellImageData.GetPixelFormat, IShellImageData::GetPixelFormat, _shell_IShellImageData_GetPixelFormat, shell.IShellImageData_GetPixelFormat, shimgdata/IShellImageData::GetPixelFormat
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
req.typenames: SHELL_UI_COMPONENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellImageData.GetPixelFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::GetPixelFormat


## -description


Gets the pixel format of the image.


## -parameters




### -param pFormat [out]

Type: <b>PixelFormat*</b>

A pointer to a value of type <a href="_gdiplus_CONSTANT_Image_Pixel_Format_Constants">PixelFormat</a> indicating the pixel format.  This value is valid only when the method returns <b>S_OK</b>.


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
The image has not been decoded or the decoding process failed.

</td>
</tr>
</table>
 




## -remarks



Values that identify various pixel formats are defined in Gdipluspixelformats.h.



