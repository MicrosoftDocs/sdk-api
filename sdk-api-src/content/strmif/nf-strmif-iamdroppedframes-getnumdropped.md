---
UID: NF:strmif.IAMDroppedFrames.GetNumDropped
title: IAMDroppedFrames::GetNumDropped
author: windows-sdk-content
description: The GetNumDropped method retrieves the total number of frames that the filter has dropped since it started streaming.
old-location: dshow\iamdroppedframes_getnumdropped.htm
old-project: DirectShow
ms.assetid: d7e91efb-0755-4319-ac85-abc6ecdc3e2a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetNumDropped, GetNumDropped method [DirectShow], GetNumDropped method [DirectShow],IAMDroppedFrames interface, IAMDroppedFrames interface [DirectShow],GetNumDropped method, IAMDroppedFrames.GetNumDropped, IAMDroppedFrames::GetNumDropped, IAMDroppedFramesGetNumDropped, dshow.iamdroppedframes_getnumdropped, strmif/IAMDroppedFrames::GetNumDropped
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDroppedFrames.GetNumDropped
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDroppedFrames::GetNumDropped


## -description



The <code>GetNumDropped</code> method retrieves the total number of frames that the filter has dropped since it started streaming.




## -parameters




### -param plDropped [out]

Pointer to a variable that receives the number of dropped frames.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



The filter resets the count to zero when it transitions from stopped to paused.

If your application uses the <a href="https://msdn.microsoft.com/126c7ed7-acc0-4248-a3ab-c91c9f1c5cee">IAMStreamControl</a> interface to control a pin, the driver might continue to count dropped and non-dropped frames while the pin is off. To get an accurate count, call this method once when you turn on the pin, and again when you turn off the pin. The difference is the total number of dropped frames. (If the start time occurs later than the call to <a href="https://msdn.microsoft.com/ce155b83-ee4a-47d4-9258-a1d18cf25f8b">IAMStreamControl::StartAt</a>, the application should listen for the <a href="https://msdn.microsoft.com/e2f8d9a2-c96c-457c-8a88-7c86d4405928">EC_STREAM_CONTROL_STARTED</a> event.) These remarks also apply if your application uses the <a href="https://msdn.microsoft.com/f5c91444-6ddb-403c-bff5-33d9ce91fae3">ICaptureGraphBuilder2::ControlStream</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b41c3792-76fe-48e0-b2f5-ca3b0ee4c8ae">IAMDroppedFrames Interface</a>
 

 

