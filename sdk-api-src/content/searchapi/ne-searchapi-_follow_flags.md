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

# _FOLLOW_FLAGS enumeration


## -description


Used to help define behavior when crawling or indexing.  These flags are used by the <a href="https://msdn.microsoft.com/948549da-7179-4f8d-956e-4daf20f8c65a">ISearchCrawlScopeManager::AddDefaultScopeRule</a> and
<a href="https://msdn.microsoft.com/100bf0b4-553c-4ecd-a40d-ee2948f2c4d5">ISearchCrawlScopeManager::AddUserScopeRule</a> methods.


## -enum-fields




### -field FF_INDEXCOMPLEXURLS

Specifies whether complex URLs (those containing a '?') should be indexed.


### -field FF_SUPPRESSINDEXING

Follow but do not index this URL.

