---
UID: NF:strmif.IDDrawExclModeVideo.GetDDrawSurface
title: IDDrawExclModeVideo::GetDDrawSurface
author: windows-sdk-content
description: The GetDDrawSurface method retrieves the DirectDraw surface being used by the Overlay Mixer.
old-location: dshow\iddrawexclmodevideo_getddrawsurface.htm
old-project: DirectShow
ms.assetid: 0fb29af3-5f6f-4502-8785-72c64f72fec4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetDDrawSurface, GetDDrawSurface method [DirectShow], GetDDrawSurface method [DirectShow],IDDrawExclModeVideo interface, IDDrawExclModeVideo interface [DirectShow],GetDDrawSurface method, IDDrawExclModeVideo.GetDDrawSurface, IDDrawExclModeVideo::GetDDrawSurface, IDDrawExclModeVideoGetDDrawSurface, dshow.iddrawexclmodevideo_getddrawsurface, strmif/IDDrawExclModeVideo::GetDDrawSurface
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
 - IDDrawExclModeVideo.GetDDrawSurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDDrawExclModeVideo::GetDDrawSurface


## -description



The <code>GetDDrawSurface</code> method retrieves the DirectDraw surface being used by the Overlay Mixer.




## -parameters




### -param ppDDrawSurface




### -param pbUsingExternal






#### - pDDrawSurface [out]

Address of a pointer to the <b>IDirectDrawSurface</b> interface that is being used by the Overlay Mixer.


#### - pdUsingExternal [out]

Pointer to a variable that receives a Boolean value. It receives the value <b>TRUE</b> if the Overlay Mixer is using a DirectDraw surface specified by <a href="https://msdn.microsoft.com/a897c147-044d-44e2-9029-bd62c74483d2">IDDrawExclModeVideo::SetDDrawSurface</a>, or <b>FALSE</b> otherwise.


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
<tr>
<td width="40%">
<dl>
<dt><b>A DirectDraw error code</b></dt>
</dl>
</td>
<td width="60%">
A DirectDraw error is encountered when trying to set the specified surface on the Overlay Mixer.

</td>
</tr>
</table>
 




## -remarks



If the filter graph has not set a DirectDraw surface and the Overlay Mixer has not yet allocated one, then <i>pDDrawSurface</i> will be set to <b>NULL</b> and <i>pdUsingExternal</i> will be set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

