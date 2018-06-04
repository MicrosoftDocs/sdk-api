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

# GetMediaComponentPackageInfo function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Returns a list of properties for all media codecs installed on the system that meet the specified requirements.


## -parameters




### -param trustedOnly [in]

True if the query should only return properties for packages that run in the app's process space; false if the query should include packages that run in  a separate app service.


### -param category [in]

A string that specifies the category of packages that should be included in the results.


### -param codecPropertiesVector [out]

A list of <a href="https://msdn.microsoft.com/9fd38910-0ee6-4cbd-9dcf-ac7129d2c911">IPropertySet</a> objects representing the properties of the installed media component packages that meet the specified criteria.


## -returns



Returns S_OK on successful completion.



