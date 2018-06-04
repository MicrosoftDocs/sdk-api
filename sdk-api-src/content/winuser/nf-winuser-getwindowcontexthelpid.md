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

# GetWindowContextHelpId function


## -description


Retrieves the Help context identifier, if any, associated with the specified window.


## -parameters




### -param Arg1

TBD




#### - hwnd

Type: <b>HWND</b>

A handle to the window for which the Help context identifier is to be retrieved.


## -returns



Type: <b>DWORD</b>

Returns the Help context identifier if the window has one, or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7e0963d1-5807-4db5-9abf-cdb21a03b525">SetWindowContextHelpId</a>
 

 

