---
UID: NF:shlobj_core.IShellIconOverlay.GetOverlayIconIndex
title: IShellIconOverlay::GetOverlayIconIndex
author: windows-sdk-content
description: Gets the index of the icon overlay in the system image list.
old-location: shell\IShellIconOverlay_GetOverlayIconIndex.htm
tech.root: shell
ms.assetid: ae7c55a1-8540-44d3-9793-2d6ac849ef60
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOverlayIconIndex, GetOverlayIconIndex method [Windows Shell], GetOverlayIconIndex method [Windows Shell],IShellIconOverlay interface, IShellIconOverlay interface [Windows Shell],GetOverlayIconIndex method, IShellIconOverlay.GetOverlayIconIndex, IShellIconOverlay::GetOverlayIconIndex, _win32_IShellIconOverlay_GetOverlayIconIndex, shell.IShellIconOverlay_GetOverlayIconIndex, shlobj_core/IShellIconOverlay::GetOverlayIconIndex
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
 - IShellIconOverlay.GetOverlayIconIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellIconOverlay::GetOverlayIconIndex


## -description


Gets the index of the icon overlay in the system image list.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

Pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that identifies the object whose icon is being displayed.


### -param pIconIndex [in, out]

Type: <b>int*</b>

Pointer to the index of the icon overlay's image in the system image list. This index is equivalent to the <i>iImage</i> value that is specified when you add an overlay image to a private image list with the <a href="https://msdn.microsoft.com/en-us/library/Bb775227(v=VS.85).aspx">ImageList::SetOverlayImage</a> function.


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
</table>
 




## -remarks



To retrieve the overlay's image index in the system image list, you must first call <a href="https://msdn.microsoft.com/20001ae0-05d0-46a7-8bb8-9bb722f5d795">SHGetIconOverlayIndex</a> to retrieve the overlay index. Then use the <a href="https://msdn.microsoft.com/en-us/library/Bb761408(v=VS.85).aspx">INDEXTOOVERLAYMASK</a> macro to convert the overlay index into the equivalent image index.




## -see-also




<a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>
 

 

