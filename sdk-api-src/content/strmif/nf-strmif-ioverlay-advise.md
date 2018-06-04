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

# IOverlay::Advise


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
 

 

