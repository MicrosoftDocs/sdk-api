---
UID: NF:strmif.IDDrawExclModeVideo.GetDDrawObject
title: IDDrawExclModeVideo::GetDDrawObject
author: windows-sdk-content
description: The GetDDrawObject method retrieves the DirectDraw object being used by the Overlay Mixer filter.
old-location: dshow\iddrawexclmodevideo_getddrawobject.htm
tech.root: DirectShow
ms.assetid: b664fbcc-de14-42ca-95d0-97719e381605
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDDrawObject, GetDDrawObject method [DirectShow], GetDDrawObject method [DirectShow],IDDrawExclModeVideo interface, IDDrawExclModeVideo interface [DirectShow],GetDDrawObject method, IDDrawExclModeVideo.GetDDrawObject, IDDrawExclModeVideo::GetDDrawObject, IDDrawExclModeVideoGetDDrawObject, dshow.iddrawexclmodevideo_getddrawobject, strmif/IDDrawExclModeVideo::GetDDrawObject
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
 - IDDrawExclModeVideo.GetDDrawObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDDrawExclModeVideo::GetDDrawObject


## -description



The <code>GetDDrawObject</code> method retrieves the DirectDraw object being used by the Overlay Mixer filter.




## -parameters




### -param ppDDrawObject [out]

Address of a pointer to the <b>IDirectDraw</b> interface that the Overlay Mixer is using.


### -param pbUsingExternal [out]

Pointer to a variable that receives a Boolean value. It receives the value <b>TRUE</b> if the Overlay Mixer is using a DirectDraw object specified by <a href="https://msdn.microsoft.com/fce1b5df-c3df-475c-adde-392c25d05e4c">IDDrawExclModeVideo::SetDDrawObject</a>, or <b>FALSE</b> otherwise.


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



If the filter graph has not set a DirectDraw object and the Overlay Mixer has not yet allocated one, then <i>pDDrawObject</i> will be set to <b>NULL</b> and <i>pbUsingExternal</i> will be set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a846a07-f513-49e7-85e8-192a5c211515">IDDrawExclModeVideo Interface</a>
 

 

