---
UID: NF:shimgdata.IShellImageData.Draw
title: IShellImageData::Draw
author: windows-sdk-content
description: Draws a decoded image.
old-location: shell\IShellImageData_Draw.htm
tech.root: shell
ms.assetid: 35989c3b-15b9-4503-a883-99df730b2a80
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Draw, Draw method [Windows Shell], Draw method [Windows Shell],IShellImageData interface, IShellImageData interface [Windows Shell],Draw method, IShellImageData.Draw, IShellImageData::Draw, _shell_IShellImageData_Draw, shell.IShellImageData_Draw, shimgdata/IShellImageData::Draw
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
 - IShellImageData.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellImageData::Draw


## -description


Draws a decoded image.


## -parameters




### -param hdc [in]

Type: <b>HDC</b>

The handle of the image.


### -param prcDest [in]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>, measured in pixels, that specifies the bounds of the rendered image. The portion of the image specified by <i>prcSrc</i> is scaled to fill the rectangle specified by <i>prcDest</i>.


### -param prcSrc [in]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> that specifies the portion of the image to be drawn.


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
The image was not previously decoded, the call to <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">IShellImageData::Decode</a> failed, or <i>hdc</i> is <b>NULL</b>. Other internal calls also can cause this error to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>prcDest</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The process was terminated by the calling application through a registered instance of <a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>.

</td>
</tr>
</table>
 




## -remarks



If <i>prcSrc</i> is <b>NULL</b>, nothing is drawn and the method returns S_OK.



