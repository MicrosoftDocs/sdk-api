---
UID: NF:amaudio.IAMDirectSound.SetFocusWindow
title: IAMDirectSound::SetFocusWindow
author: windows-driver-content
description: The SetFocusWindow method specifies a window to handle sound playback.
old-location: dshow\iamdirectsound_setfocuswindow.htm
old-project: DirectShow
ms.assetid: 3fc9dbb3-83bb-4c46-8ada-a7b7b8a784fe
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMDirectSound interface [DirectShow],SetFocusWindow method, IAMDirectSound.SetFocusWindow, IAMDirectSound::SetFocusWindow, IAMDirectSoundSetWindowFocus, SetFocusWindow, SetFocusWindow method [DirectShow], SetFocusWindow method [DirectShow],IAMDirectSound interface, amaudio/IAMDirectSound::SetFocusWindow, dshow.iamdirectsound_setfocuswindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amaudio.h
req.include-header: 
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
req.typenames: SOCKADDR_IRDA, *PSOCKADDR_IRDA, *LPSOCKADDR_IRDA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMDirectSound.SetFocusWindow
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMDirectSound::SetFocusWindow


## -description



The <code>SetFocusWindow</code> method specifies a window to handle sound playback.




## -parameters




### -param






#### - bMixingOnOrOff [in]

Specifies whether to mix the sound when the window loses focus.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The sound is audible when the window loses focus.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The sound is not audible when the window loses focus.</td>
</tr>
</table>
 


#### - hWnd [in]

Specifies a handle to the window. If this value is <b>NULL</b>, the sound will not be associated with any window.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28">IAMDirectSound Interface</a>
 

 

