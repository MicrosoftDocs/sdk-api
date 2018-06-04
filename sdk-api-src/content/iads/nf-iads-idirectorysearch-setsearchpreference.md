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

# IDirectorySearch::SetSearchPreference


## -description


The <b>IDirectorySearch::SetSearchPreference</b> method specifies a search preference for obtaining data in a subsequent search.


## -parameters




### -param pSearchPrefs [in]

Provides a caller-allocated array of  <a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a> structures that contain the search preferences to be set.


### -param dwNumPrefs [in]

Provides the size of the <i>pSearchPrefs</i> array.


## -returns



This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/5fc46271-a1be-4a9d-a340-ed801211736a">ADS_SEARCHPREF_INFO</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

