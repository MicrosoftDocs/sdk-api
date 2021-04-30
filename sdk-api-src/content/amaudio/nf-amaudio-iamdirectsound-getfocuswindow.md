---
UID: NF:amaudio.IAMDirectSound.GetFocusWindow
title: IAMDirectSound::GetFocusWindow (amaudio.h)
description: The GetFocusWindow method retrieves the window that is handling sound playback.
helpviewer_keywords: ["GetFocusWindow","GetFocusWindow method [DirectShow]","GetFocusWindow method [DirectShow]","IAMDirectSound interface","IAMDirectSound interface [DirectShow]","GetFocusWindow method","IAMDirectSound.GetFocusWindow","IAMDirectSound::GetFocusWindow","IAMDirectSoundGetWindowFocus","amaudio/IAMDirectSound::GetFocusWindow","dshow.iamdirectsound_getfocuswindow"]
old-location: dshow\iamdirectsound_getfocuswindow.htm
tech.root: dshow
ms.assetid: e103abb3-01fc-452f-a151-0f2d24859fba
ms.date: 12/05/2018
ms.keywords: GetFocusWindow, GetFocusWindow method [DirectShow], GetFocusWindow method [DirectShow],IAMDirectSound interface, IAMDirectSound interface [DirectShow],GetFocusWindow method, IAMDirectSound.GetFocusWindow, IAMDirectSound::GetFocusWindow, IAMDirectSoundGetWindowFocus, amaudio/IAMDirectSound::GetFocusWindow, dshow.iamdirectsound_getfocuswindow
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
 - IAMDirectSound::GetFocusWindow
 - amaudio/IAMDirectSound::GetFocusWindow
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
 - IAMDirectSound.GetFocusWindow
---

# IAMDirectSound::GetFocusWindow


## -description

The <code>GetFocusWindow</code> method retrieves the window that is handling sound playback.

## -parameters

### -param unnamedParam1 [out]

Pointer to a variable that receives a handle to the window. If sound playback is not associated with a window, the returned value is <b>NULL</b>.

### -param unnamedParam2 [out]

Pointer to a variable that receives one of the following values.

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

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amaudio/nn-amaudio-iamdirectsound">IAMDirectSound Interface</a>