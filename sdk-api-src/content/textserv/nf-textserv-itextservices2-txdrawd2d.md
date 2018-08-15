---
UID: NF:textserv.ITextServices2.TxDrawD2D
title: ITextServices2::TxDrawD2D
author: windows-sdk-content
description: Draws the text services object by using Direct2D rendering.
old-location: controls\itextservices2_txdrawd2d.htm
old-project: controls
ms.assetid: B45B015A-0A2C-49DD-9AA9-FC2A530BD057
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextServices2 interface [Windows Controls],TxDrawD2D method, ITextServices2.TxDrawD2D, ITextServices2::TxDrawD2D, TXTVIEW_ACTIVE, TXTVIEW_INACTIVE, TxDrawD2D, TxDrawD2D method [Windows Controls], TxDrawD2D method [Windows Controls],ITextServices2 interface, controls.itextservices2_txdrawd2d, textserv/ITextServices2::TxDrawD2D
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices2.TxDrawD2D
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

