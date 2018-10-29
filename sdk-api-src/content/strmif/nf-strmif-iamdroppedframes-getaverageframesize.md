---
UID: NF:strmif.IAMDroppedFrames.GetAverageFrameSize
title: IAMDroppedFrames::GetAverageFrameSize
author: windows-sdk-content
description: The GetAverageFrameSize method retrieves the average size of the frames that the filter has captured.
old-location: dshow\iamdroppedframes_getaverageframesize.htm
tech.root: DirectShow
ms.assetid: 49b63a9f-8192-4fce-8cfe-c92bd39ca2b0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetAverageFrameSize, GetAverageFrameSize method [DirectShow], GetAverageFrameSize method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetAverageFrameSize method, IAMDroppedFrames.GetAverageFrameSize, IAMDroppedFrames::GetAverageFrameSize, IAMDroppedFramesGetAverageFrameSize, dshow.iamdroppedframes_getaverageframesize, strmif/IAMDroppedFrames::GetAverageFrameSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDroppedFrames.GetAverageFrameSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDroppedFrames::GetAverageFrameSize


## -description



The <code>GetAverageFrameSize</code> method retrieves the average size of the frames that the filter has captured.




## -parameters




### -param plAverageSize [out]

Pointer to a variable that receives the average frame size, in bytes, since the filter began streaming.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



If the device does not report a value, the method might succeed but return zero in the <i>plAverageSize</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b41c3792-76fe-48e0-b2f5-ca3b0ee4c8ae">IAMDroppedFrames Interface</a>
 

 

