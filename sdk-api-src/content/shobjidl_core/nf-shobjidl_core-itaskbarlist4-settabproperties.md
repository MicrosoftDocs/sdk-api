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

# ITaskbarList4::SetTabProperties


## -description


Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window that is to have properties set. This handle must already be registered through <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">RegisterTab</a>.


### -param stpFlags [in]

Type: <b><a href="https://msdn.microsoft.com/7d50e4fe-1689-4dbd-b367-f4881d8d5d78">STPFLAG</a></b>

One or more members of the <a href="https://msdn.microsoft.com/7d50e4fe-1689-4dbd-b367-f4881d8d5d78">STPFLAG</a> enumeration that specify the displayed thumbnail and peek image source of the tab thumbnail.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application might want to use the thumbnail or peek representation of its associated parent window if the application cannot generate its own thumbnail for a tab or for its active tab content (such as an animation) to appear live.




## -see-also




<a href="https://msdn.microsoft.com/7fc2c615-0bb0-4c03-9775-eee566c71088">ITaskbarList4</a>
 

 

