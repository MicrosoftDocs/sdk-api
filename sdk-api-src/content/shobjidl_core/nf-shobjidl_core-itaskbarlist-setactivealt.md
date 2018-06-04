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

# ITaskbarList::SetActiveAlt


## -description


Marks a taskbar item as active but does not visually activate it.


## -parameters




### -param hwnd

Type: <b>HWND</b>

A handle to the window to be marked as active.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SetActiveAlt</b> marks the item associated with <i>hwnd</i> as the currently active item for the window's process without changing the pressed state of any item. Any user action that would activate a different tab in that process will activate the tab associated with <i>hwnd</i> instead. The active state of the window's item is not guaranteed to be preserved when the process associated with <i>hwnd</i> is not active. To ensure that a given tab is always active, call <b>SetActiveAlt</b> whenever any of your windows are activated. Calling <b>SetActiveAlt</b> with a <b>NULL</b> <i>hwnd</i> clears this state.



