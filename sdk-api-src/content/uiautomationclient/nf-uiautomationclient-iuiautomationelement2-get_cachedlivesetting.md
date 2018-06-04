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

# IUIAutomationElement2::get_CachedLiveSetting


## -description


Retrieves a cached value that indicates the type of notifications, if any, that the element sends when the content of the element changes. 

This property is read-only.


## -parameters


## -remarks



This property maps to the Accessible Rich Internet Applications (ARIA)<b> live</b> property.

The LiveSetting property is supported by provider elements that are part of a live region. When the content of a live region changes, the provider element can raise a notification. A client application determines whether to notify the user of the changes based on the value of the LiveSetting property.




## -see-also




<a href="https://msdn.microsoft.com/3510E0AD-FB79-4636-B6EF-AE0FB62AD55C">CurrentLiveSetting</a>



<a href="https://msdn.microsoft.com/4D9A4E94-BAE9-4E85-8F21-7CABFBE64C6D">IUIAutomationElement2</a>



<a href="https://msdn.microsoft.com/40DD1F00-A9BC-4C84-B2A3-940E37EE9C19">LiveSetting</a>
 

 

