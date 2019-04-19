---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateColorKey
title: IDDrawExclModeVideoCallback::OnUpdateColorKey (strmif.h)
author: windows-sdk-content
description: The OnUpdateColorKey method informs the application that the color key has changed so that the application can use the new color key to overlay graphics on the video.
old-location: dshow\iddrawexclmodevideocallback_onupdatecolorkey.htm
tech.root: DirectShow
ms.assetid: 87d4a4b5-f67e-46f6-956a-1c9c309bfde7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateColorKey method, IDDrawExclModeVideoCallback.OnUpdateColorKey, IDDrawExclModeVideoCallback::OnUpdateColorKey, IDDrawExclModeVideoCallbackOnUpdateColorKey, OnUpdateColorKey, OnUpdateColorKey method [DirectShow], OnUpdateColorKey method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdatecolorkey, strmif/IDDrawExclModeVideoCallback::OnUpdateColorKey
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
 - IDDrawExclModeVideoCallback.OnUpdateColorKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDDrawExclModeVideoCallback::OnUpdateColorKey


## -description



The <code>OnUpdateColorKey</code> method informs the application that the color key has changed so that the application can use the new color key to overlay graphics on the video.




## -parameters




### -param pKey [out]

Pointer to a <a href="https://msdn.microsoft.com/1563488a-e4e5-472d-b665-5bbcb13fad1a">COLORKEY</a> structure that contains the key type and a palette index.


### -param dwColor [out]

Value indicating the 8-bit palette index of the <b>COLORKEY</b> returned in <i>pKey</i>, if the current display mode is 8-bit palettized. Otherwise, it is a value representing the color key in the pixel format of the current display mode.


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
One of the parameters is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback Interface</a>
 

 

