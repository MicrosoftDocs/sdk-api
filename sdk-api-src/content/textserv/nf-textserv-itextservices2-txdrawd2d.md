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

# ITextServices2::TxDrawD2D


## -description


Draws the text services object by using Direct2D rendering.


## -parameters




### -param pRenderTarget

Type: <b><a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>*</b>

The Direct2D rendering object that draws the text services object.


### -param lprcBounds

Type: <b><a href="https://msdn.microsoft.com/47a89d2d-4733-47be-91c1-450845e78075">LPCRECTL</a></b>

The bounding (client) rectangle.


### -param lprcUpdate

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">LPRECT</a></b>

The rectangle to update inside <i>lprcBounds</i> rectangle, in the logical coordinate system of drawing device context. If this parameter is NULL, the entire client rectangle should be drawn. 



### -param lViewId

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The view to draw.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_ACTIVE"></a><a id="txtview_active"></a><dl>
<dt><b>TXTVIEW_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw the in-place   active view.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTVIEW_INACTIVE"></a><a id="txtview_inactive"></a><dl>
<dt><b>TXTVIEW_INACTIVE</b></dt>
</dl>
</td>
<td width="60%">
Draw a view other than the in-place active view, for example, a print    preview. 

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B5DC90BA-F9A5-45DC-8C8A-784380C38769">ITextServices2</a>
 

 

