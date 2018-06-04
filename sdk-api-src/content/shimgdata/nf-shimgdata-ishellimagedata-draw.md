---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>, measured in pixels, that specifies the bounds of the rendered image. The portion of the image specified by <i>prcSrc</i> is scaled to fill the rectangle specified by <i>prcDest</i>.


### -param prcSrc [in]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> that specifies the portion of the image to be drawn.


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



