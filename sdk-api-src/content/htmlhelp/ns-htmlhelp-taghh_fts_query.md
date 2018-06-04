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

# tagHH_FTS_QUERY structure


## -description


Use this structure for full-text search. 


## -struct-fields




### -field cbStruct

Specifies the size of the structure. 


### -field fUniCodeStrings

TRUE if all strings are Unicode. 


### -field pszSearchQuery

String containing the search query. 


### -field iProximity

Word proximity. 


### -field fStemmedSearch

TRUE for StemmedSearch only. 


### -field fTitleOnly

TRUE for Title search only. 


### -field fExecute

TRUE to initiate the search. 


### -field pszWindow

Window to display in. 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About Structures</a>
 

 

