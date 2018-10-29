---
UID: NF:amaudio.IAMDirectSound.GetFocusWindow
title: IAMDirectSound::GetFocusWindow
author: windows-sdk-content
description: The GetFocusWindow method retrieves the window that is handling sound playback.
old-location: dshow\iamdirectsound_getfocuswindow.htm
tech.root: DirectShow
ms.assetid: e103abb3-01fc-452f-a151-0f2d24859fba
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetFocusWindow, GetFocusWindow method [DirectShow], GetFocusWindow method [DirectShow],IAMDirectSound interface, IAMDirectSound interface [DirectShow],GetFocusWindow method, IAMDirectSound.GetFocusWindow, IAMDirectSound::GetFocusWindow, IAMDirectSoundGetWindowFocus, amaudio/IAMDirectSound::GetFocusWindow, dshow.iamdirectsound_getfocuswindow
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
 - IAMDirectSound.GetFocusWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMDirectSound::GetFocusWindow


## -description



The <code>GetFocusWindow</code> method retrieves the window that is handling sound playback.




## -parameters




### -param arg1 [out]

Pointer to a variable that receives a handle to the window. If sound playback is not associated with a window, the returned value is <b>NULL</b>.


### -param arg2 [out]

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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a9afaeb7-e2d4-4dbf-9f4d-144cafbd5e28">IAMDirectSound Interface</a>
 

 

