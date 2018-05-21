---
UID: NF:strmif.IDDrawExclModeVideo.SetDDrawObject
title: IDDrawExclModeVideo::SetDDrawObject
author: windows-driver-content
description: The SetDDrawObject method sets the DirectDraw object to be used in subsequent drawing.
old-location: dshow\iddrawexclmodevideo_setddrawobject.htm
old-project: DirectShow
ms.assetid: fce1b5df-c3df-475c-adde-392c25d05e4c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDDrawObject method, IDDrawExclModeVideo.SetDDrawObject, IDDrawExclModeVideo::SetDDrawObject, IDDrawExclModeVideoSetDDrawObject, SetDDrawObject, SetDDrawObject method [DirectShow], SetDDrawObject method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setddrawobject, strmif/IDDrawExclModeVideo::SetDDrawObject
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDDrawExclModeVideo.SetDDrawObject
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDDrawExclModeVideo::SetDDrawObject


## -description



The <code>SetDDrawObject</code> method sets the DirectDraw object to be used in subsequent drawing.




## -parameters




### -param pDDrawObject [in]

Pointer to the <b>IDirectDraw</b> interface on the object to use.


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



A game application can use this method to share its DirectDraw object with the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter, so that the video can be drawn in a specified surface, as set in <a href="https://msdn.microsoft.com/a897c147-044d-44e2-9029-bd62c74483d2">IDDrawExclModeVideo::SetDDrawSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

