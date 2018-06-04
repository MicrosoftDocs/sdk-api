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

# __MIDL___MIDL_itf_searchapi_0000_0013_0001 enumeration


## -description


These flags enumerate reasons why URLs are included or excluded from the current crawl scope. The 
<a href="https://msdn.microsoft.com/018c240b-491c-4974-8059-ee7331672e6b">ISearchCrawlScopeManager::IncludedInCrawlScopeEx</a> method returns a pointer to this enumeration to explain why a specified URL is either included or excluded from the current crawl scope.


## -enum-fields




### -field CLUSIONREASON_UNKNOWNSCOPE

The URL has been excluded because its scope in unknown. There is no scope that would include or exclude this URL so it is excluded by default.


### -field CLUSIONREASON_DEFAULT

The URL has been included or excluded by a default rule. Default rules are set during setup or first run.


### -field CLUSIONREASON_USER

The URL has been included or excluded by a user rule. User rules are set either by the user through Control Panel or by a calling application through the <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface.


### -field CLUSIONREASON_GROUPPOLICY

 Not Supported.

