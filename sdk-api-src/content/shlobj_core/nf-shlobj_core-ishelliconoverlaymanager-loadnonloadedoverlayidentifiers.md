---
UID: NF:shlobj_core.IShellIconOverlayManager.LoadNonloadedOverlayIdentifiers
title: IShellIconOverlayManager::LoadNonloadedOverlayIdentifiers (shlobj_core.h)
author: windows-sdk-content
description: Loads any registered overlay identifiers, or handlers, that are not currently loaded.
old-location: shell\IShellIconOverlayManager_LoadNonloadedOverlayIdentifiers.htm
tech.root: shell
ms.assetid: bd6003b5-551d-41cc-8ca6-13ab245ed6fd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellIconOverlayManager interface [Windows Shell],LoadNonloadedOverlayIdentifiers method, IShellIconOverlayManager.LoadNonloadedOverlayIdentifiers, IShellIconOverlayManager::LoadNonloadedOverlayIdentifiers, LoadNonloadedOverlayIdentifiers, LoadNonloadedOverlayIdentifiers method [Windows Shell], LoadNonloadedOverlayIdentifiers method [Windows Shell],IShellIconOverlayManager interface, _win32_IShellIconOverlayManager_LoadNonloadedOverlayIdentifiers, shell.IShellIconOverlayManager_LoadNonloadedOverlayIdentifiers, shlobj_core/IShellIconOverlayManager::LoadNonloadedOverlayIdentifiers
ms.topic: method
req.header: shlobj_core.h
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
 - IShellIconOverlayManager.LoadNonloadedOverlayIdentifiers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellIconOverlayManager::LoadNonloadedOverlayIdentifiers


## -description


Loads any registered overlay identifiers, or handlers, that are not currently loaded.


## -parameters






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
Not out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/769c3b0b-ece4-4406-a76c-cabc37901351">IShellIconOverlayManager</a>
 

 

