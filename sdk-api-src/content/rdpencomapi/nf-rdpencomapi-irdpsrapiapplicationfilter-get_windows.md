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

# IRDPSRAPIApplicationFilter::get_Windows


## -description


The list of sharable windows.

This property is read-only.


## -parameters


## -remarks



The window objects are also available through the list returned by <a href="https://msdn.microsoft.com/6e6cf29d-e19a-43bd-a4e7-993c10bac92b">IRDPSRAPIApplication::Windows</a>. The windows are also exposed by the application filter because it provides easy access to all windows in the session, especially for applications that share only at the window level.




## -see-also




<a href="https://msdn.microsoft.com/6a08c948-1b25-4a36-93c8-23e7e3f4fb08">IRDPSRAPIApplicationFilter</a>
 

 

