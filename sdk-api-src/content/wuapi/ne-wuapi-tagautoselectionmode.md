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

# tagAutoSelectionMode enumeration


## -description


Defines  the types of logic that is used to determine whether a particular update will be automatically selected when the user views  available updates in the Windows Update user interface.


## -enum-fields




### -field asLetWindowsUpdateDecide

Use the standard logic. The update will be automatically selected if it is important, or if it is recommended and Windows Update has been configured to treat recommended updates as important. Otherwise, the update will not be automatically selected.


### -field asAutoSelectIfDownloaded

The update will be automatically selected only if it has been completely downloaded.


### -field asNeverAutoSelect

The update will never be automatically selected.


### -field asAlwaysAutoSelect

The update will always be automatically selected.


## -remarks



In versions of the Windows Update Agent (WUA) in which <a href="https://msdn.microsoft.com/ff290e39-7d7c-42da-a522-ba9e672721b8">IUpdate5</a> is not available, all updates are processed by using the standard logic.



