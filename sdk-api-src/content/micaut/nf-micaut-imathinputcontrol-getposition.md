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

# IMathInputControl::GetPosition


## -description


Retrieves the position and size of the control.


## -parameters




### -param Left [out]

The leftmost position of the control.


### -param Top [out]

The highest position of the control.


### -param Right [out]

The rightmost position of the control.


### -param Bottom [out]

The lowest position of the control.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the control size and position even if the control is not visible.

This method returns the minimal possible width and height of the control if it is  called immediatelly after creation of the control.




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>



<a href="https://msdn.microsoft.com/9b5fc988-7c93-47d4-8661-4cef56cab0d0">SetPosition</a>
 

 

