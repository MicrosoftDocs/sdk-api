---
UID: NF:shimgdata.IShellImageData.Scale
title: IShellImageData::Scale
author: windows-driver-content
description: Adjusts the size of an image.
old-location: shell\IShellImageData_Scale.htm
old-project: shell
ms.assetid: ebcc9cc1-b6ee-4fb9-9125-54d6a9ee9434
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IShellImageData interface [Windows Shell],Scale method, IShellImageData.Scale, IShellImageData::Scale, Scale, Scale method [Windows Shell], Scale method [Windows Shell],IShellImageData interface, _shell_IShellImageData_Scale, shell.IShellImageData_Scale, shimgdata/IShellImageData::Scale
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
-	IShellImageData.Scale
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellImageData::Scale


## -description


Adjusts the size of an image.


## -parameters




### -param cx [in]

Type: <b>ULONG</b>

The horizontal (x) dimension. If this value is 0, the x dimension is set to a scaled value based on the point specified in <i>cy</i>.


### -param cy [in]

Type: <b>ULONG</b>

The vertical (y) dimension. If this value is 0, the y dimension is set to a scaled value based on the point specified in <i>cx</i>.


### -param hints [in]

Type: <b><a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a></b>

A member of the <a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a> enumeration, specifying the algorithm that is used when the image is scaled.


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
The image was not previously decoded or the call to <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">IShellImageData::Decode</a> failed. Other internal calls also can cause this error to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTVALIDFORANIMATEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image is an animated image and cannot be scaled using this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The process was stopped by the calling application through a registered instance of <a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>.

</td>
</tr>
</table>
 



