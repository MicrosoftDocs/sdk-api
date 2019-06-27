---
UID: NF:amaudio.IAMDirectSound.SetFocusWindow
title: IAMDirectSound::SetFocusWindow (amaudio.h)
author: windows-sdk-content
description: The SetFocusWindow method specifies a window to handle sound playback.
old-location: dshow\iamdirectsound_setfocuswindow.htm
tech.root: DirectShow
ms.assetid: 3fc9dbb3-83bb-4c46-8ada-a7b7b8a784fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMDirectSound interface [DirectShow],SetFocusWindow method, IAMDirectSound.SetFocusWindow, IAMDirectSound::SetFocusWindow, IAMDirectSoundSetWindowFocus, SetFocusWindow, SetFocusWindow method [DirectShow], SetFocusWindow method [DirectShow],IAMDirectSound interface, amaudio/IAMDirectSound::SetFocusWindow, dshow.iamdirectsound_setfocuswindow
ms.topic: method
f1_keywords: 
 - "amaudio/IAMDirectSound.SetFocusWindow"
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
 - IAMDirectSound.SetFocusWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDirectSound::SetFocusWindow


## -description



The <code>SetFocusWindow</code> method specifies a window to handle sound playback.




## -parameters




### -param arg1 [in]

Specifies a handle to the window. If this value is <b>NULL</b>, the sound will not be associated with any window.


### -param arg2 [in]

Specifies whether to mix the sound when the window loses focus.

<table>
<tr>
<th>Value
                </th>
<th>Description
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
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amaudio/nn-amaudio-iamdirectsound">IAMDirectSound Interface</a>
 

 

