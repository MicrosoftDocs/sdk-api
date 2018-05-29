---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateOverlay
title: IDDrawExclModeVideoCallback::OnUpdateOverlay
author: windows-sdk-content
description: The OnUpdateOverlay method informs the application when the overlay surface for the video is about to become visible, invisible, change size, or change position, so that the application can repaint its window appropriately.
old-location: dshow\iddrawexclmodevideocallback_onupdateoverlay.htm
old-project: DirectShow
ms.assetid: ede823ba-8340-4339-8e8a-e1d4f9ad1273
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateOverlay method, IDDrawExclModeVideoCallback.OnUpdateOverlay, IDDrawExclModeVideoCallback::OnUpdateOverlay, IDDrawExclModeVideoCallbackOnUpdateOverlay, OnUpdateOverlay, OnUpdateOverlay method [DirectShow], OnUpdateOverlay method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdateoverlay, strmif/IDDrawExclModeVideoCallback::OnUpdateOverlay
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
-	IDDrawExclModeVideoCallback.OnUpdateOverlay
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDDrawExclModeVideoCallback::OnUpdateOverlay


## -description



The <code>OnUpdateOverlay</code> method informs the application when the overlay surface for the video is about to become visible, invisible, change size, or change position, so that the application can repaint its window appropriately.




## -parameters




### -param bBefore




### -param dwFlags [in]

Value from the <a href="https://msdn.microsoft.com/bc16714b-acee-4b5d-aa1d-6b53965183dc">AM_OVERLAY_NOTIFY_FLAGS</a> enumeration that specifies what is about to change or what changed.


### -param bOldVisible [in]

Boolean value specifying whether the old window is visible. <b>TRUE</b> means the old window is visible.


### -param prcOldSrc




### -param prcOldDest




### -param bNewVisible [in]

Boolean specifying whether the new window is visible. <b>TRUE</b> means the new window is visible.


### -param prcNewSrc




### -param prcNewDest






#### - bBeforeChange [in]

Boolean value specifying whether the call is being made before or after the overlay-related change. <b>TRUE</b> specifies before, <b>FALSE</b> specifies after.


#### - prcDestNew [in]

Pointer to the rectangle representing the new destination position of the rectangle in the overlay surface.


#### - prcDestOld [in]

Pointer to the rectangle representing the old destination position of the rectangle in the overlay surface.


#### - prcSrcNew [in]

Pointer to the rectangle representing the new source position of the DirectDraw surface.


#### - prcSrcOld [in]

Pointer to the rectangle representing the old source position of the DirectDraw surface.


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
Invalid parameter.

</td>
</tr>
</table>
 




## -remarks



The application should call this method once before the overlay-related change occurs and once after the changes are done. In the call before the change, the overlay change doesn't happen until the application completes executing this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7f22d4cd-93e0-4d7d-b8f3-932488d2c672">IDDrawExclModeVideoCallback Interface</a>
 

 

