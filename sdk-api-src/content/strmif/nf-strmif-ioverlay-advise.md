---
UID: NF:strmif.IOverlay.Advise
title: IOverlay::Advise method
author: windows-driver-content
description: The Advise method sets up an advise link for the overlay events specified by the dwInterests parameter.
old-location: dshow\ioverlay_advise.htm
old-project: DirectShow
ms.assetid: 02db2233-b185-47a9-9655-409991a74d4e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: Advise method [DirectShow], Advise method [DirectShow], IOverlay interface, Advise,IOverlay.Advise, IOverlay, IOverlay interface [DirectShow], Advise method, IOverlay::Advise, IOverlayAdvise, dshow.ioverlay_advise, strmif/IOverlay::Advise
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
-	IOverlay.Advise
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IOverlay::Advise method


## -description



The <code>Advise</code> method sets up an advise link for the overlay events specified by the <i>dwInterests</i> parameter.




## -parameters




### -param pOverlayNotify [in]

Pointer to the notification interface.


### -param dwInterests [in]

Callbacks of interest, which can be any subset of the following events.

<table>
<tr>
<th>
                  Event
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ADVISE_NONE</td>
<td>No changes.</td>
</tr>
<tr>
<td>ADVISE_CLIPPING</td>
<td>Change in clipping region (synchronized with the window).</td>
</tr>
<tr>
<td>ADVISE_PALETTE</td>
<td>Change in palette.</td>
</tr>
<tr>
<td>ADVISE_COLORKEY</td>
<td>Change of chroma key value.</td>
</tr>
<tr>
<td>ADVISE_POSITION</td>
<td>Change in position of video window (not synchronized with the window).</td>
</tr>
<tr>
<td>ADVISE_DISPLAY_CHANGE</td>
<td>Called on <a href="https://msdn.microsoft.com/5a6111fd-648e-41a9-aaf8-e5d93f5d54cd">WM_DISPLAYCHANGE</a>. The <b>WM_DISPLAYCHANGE</b> message is sent to all windows when the display resolution has changed.</td>
</tr>
<tr>
<td>ADVISE_ALL2</td>
<td>All of the above.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method sets up an advise link for the <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> interface to receive notifications. If one of these events occurs, the appropriate entry point in the <i>pOverlayNotify</i> parameter passed in is called (<a href="https://msdn.microsoft.com/d5bed27f-2918-4c1f-9340-a0d5714d911b">IOverlayNotify::OnClipChange</a>, <a href="https://msdn.microsoft.com/a1e7fc88-a50a-4832-9b29-21b94184f1c7">IOverlayNotify::OnColorKeyChange</a>, <a href="https://msdn.microsoft.com/128e3834-d561-46d3-b32b-5bfd290f0995">IOverlayNotify::OnPaletteChange</a>, or <a href="https://msdn.microsoft.com/a5d110a6-5056-4fc1-9589-c2cc66566322">IOverlayNotify::OnPositionChange</a>).

Only one advise link can be set on any given <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> interface. Trying to set another notification interface on second and subsequent calls returns VFW_E_ADVISE_ALREADY_SET. You can cancel an advise link by using <a href="https://msdn.microsoft.com/da987152-d5cd-42c5-848a-6d70ad25ca33">IOverlay::Unadvise</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

