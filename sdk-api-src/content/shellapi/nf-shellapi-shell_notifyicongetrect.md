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

# Shell_NotifyIconGetRect function


## -description


Gets the screen coordinates of the bounding rectangle of a notification icon.


## -parameters




### -param identifier [in]

Type: <b>const <a href="https://msdn.microsoft.com/2fe4ffba-6fe5-4d34-9cb1-f266e4594b8e">NOTIFYICONIDENTIFIER</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/2fe4ffba-6fe5-4d34-9cb1-f266e4594b8e">NOTIFYICONIDENTIFIER</a> structure that identifies the icon.


### -param iconLocation [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that, when this function returns successfully, receives the coordinates of the icon.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D37E2BF7-1887-4780-81AD-85B2117321E4">Notifications and the Notification Area</a>
 

 

