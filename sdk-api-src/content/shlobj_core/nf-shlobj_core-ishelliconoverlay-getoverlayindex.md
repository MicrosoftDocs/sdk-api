---
UID: NF:shlobj_core.IShellIconOverlay.GetOverlayIndex
title: IShellIconOverlay::GetOverlayIndex
author: windows-sdk-content
description: Gets the overlay index in the system image list.
old-location: shell\IShellIconOverlay_GetOverlayIndex.htm
tech.root: shell
ms.assetid: e5bde311-8b5f-4a8b-9fff-5d062c650b95
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetOverlayIndex, GetOverlayIndex method [Windows Shell], GetOverlayIndex method [Windows Shell],IShellIconOverlay interface, IShellIconOverlay interface [Windows Shell],GetOverlayIndex method, IShellIconOverlay.GetOverlayIndex, IShellIconOverlay::GetOverlayIndex, _win32_IShellIconOverlay_GetOverlayIndex, shell.IShellIconOverlay_GetOverlayIndex, shlobj_core/IShellIconOverlay::GetOverlayIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlay.GetOverlayIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellIconOverlay::GetOverlayIndex


## -description


Gets the overlay index in the system image list.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

Pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that identifies the object whose icon is being displayed.


### -param pIndex [in, out]

Type: <b>int*</b>

Pointer to a value that states the overlay index (one-based) in the system image list. This index is equivalent to the <i>iOverlay</i> value that is specified when you add an overlay image to a private image list with the <a href="https://msdn.microsoft.com/8cb1babc-01bd-4aae-9bc7-073050242ce4">ImageList::SetOverlayImage</a> function.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
The index of an overlay was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No overlay exists for this file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The PIDL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument is invalid, for example, if <i>pIndex</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The calling application passed OI_ASYNC to signify that the operation of calculating the overlay index will take some time.

</td>
</tr>
</table>
 




## -remarks



To retrieve the overlay index in the system image list, call <a href="https://msdn.microsoft.com/20001ae0-05d0-46a7-8bb8-9bb722f5d795">SHGetIconOverlayIndex</a>.

If you set <i>pIndex</i> to point to OI_ASYNC when you call this method, the Shell icon overlay handler might return E_PENDING instead of storing the overlay index in <i>pIndex</i>. This return value indicates that computing the overlay is a slow operation and should be handled in the background. When an <a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a> implementation returns E_PENDING, it is called back on a background worker thread without the OI_ASYNC flag. If you do not use OI_ASYNC when you call <b>GetOverlayIndex</b>, the overlay handler must compute the overlay index and store the value in <i>pIndex</i> before returning.




## -see-also




<a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>
 

 

