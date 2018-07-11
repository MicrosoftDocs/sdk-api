---
UID: NF:strmif.IDDrawExclModeVideo.SetCallbackInterface
title: IDDrawExclModeVideo::SetCallbackInterface
author: windows-sdk-content
description: The SetCallbackInterface method retrieves a pointer to the callback interface of the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.
old-location: dshow\iddrawexclmodevideo_setcallbackinterface.htm
old-project: DirectShow
ms.assetid: f8f885fe-d1a2-4635-9f30-d57ac0eb905e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetCallbackInterface method, IDDrawExclModeVideo.SetCallbackInterface, IDDrawExclModeVideo::SetCallbackInterface, IDDrawExclModeVideoSetCallbackInterface, SetCallbackInterface, SetCallbackInterface method [DirectShow], SetCallbackInterface method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setcallbackinterface, strmif/IDDrawExclModeVideo::SetCallbackInterface
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
 - IDDrawExclModeVideo.SetCallbackInterface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDDrawExclModeVideo::SetCallbackInterface


## -description



The <code>SetCallbackInterface</code> method retrieves a pointer to the callback interface of the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.




## -parameters




### -param pCallback [out]

Pointer to the object that implements the <a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback</a> interface. If <i>pCallback</i> is <b>NULL</b>, the callback interface is set to <b>NULL</b> and no more callbacks are made. If there was a previous callback interface, it is released and no more callbacks are made to it. If <i>pCallback</i> is not <b>NULL</b> and this method returns S_OK, then the reference count of the object <i>pCallback</i> points to is incremented.


### -param dwFlags






#### - dwFlag [in]

Must be zero.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
</table>
 




## -remarks



An application should use this method to get notification about the overlay size, position, or color key change happening, so that it can hide or show the video, or adjust the video at the start, end, or during playback. By calling this method, an application can access the <a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback</a> interface and pass the pointer to that interface to the Overlay Mixer.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

