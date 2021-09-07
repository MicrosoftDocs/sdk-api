---
UID: NF:amaudio.IAMDirectSound.SetFocusWindow
title: IAMDirectSound::SetFocusWindow (amaudio.h)
description: The SetFocusWindow method specifies a window to handle sound playback.
helpviewer_keywords: ["IAMDirectSound interface [DirectShow]","SetFocusWindow method","IAMDirectSound.SetFocusWindow","IAMDirectSound::SetFocusWindow","IAMDirectSoundSetWindowFocus","SetFocusWindow","SetFocusWindow method [DirectShow]","SetFocusWindow method [DirectShow]","IAMDirectSound interface","amaudio/IAMDirectSound::SetFocusWindow","dshow.iamdirectsound_setfocuswindow"]
old-location: dshow\iamdirectsound_setfocuswindow.htm
tech.root: dshow
ms.assetid: 3fc9dbb3-83bb-4c46-8ada-a7b7b8a784fe
ms.date: 12/05/2018
ms.keywords: IAMDirectSound interface [DirectShow],SetFocusWindow method, IAMDirectSound.SetFocusWindow, IAMDirectSound::SetFocusWindow, IAMDirectSoundSetWindowFocus, SetFocusWindow, SetFocusWindow method [DirectShow], SetFocusWindow method [DirectShow],IAMDirectSound interface, amaudio/IAMDirectSound::SetFocusWindow, dshow.iamdirectsound_setfocuswindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMDirectSound::SetFocusWindow
 - amaudio/IAMDirectSound::SetFocusWindow
dev_langs:
 - c++
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
---

# IAMDirectSound::SetFocusWindow


## -description

The <code>SetFocusWindow</code> method specifies a window to handle sound playback.

## -parameters

### -param unnamedParam1 [in]

Specifies a handle to the window. If this value is <b>NULL</b>, the sound will not be associated with any window.

### -param unnamedParam2 [in]

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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amaudio/nn-amaudio-iamdirectsound">IAMDirectSound Interface</a>