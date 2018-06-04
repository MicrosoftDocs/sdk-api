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

# ads_search_column structure


## -description


The <b>ADS_SEARCH_COLUMN</b> structure specifies the contents of a search column in the query returned from the directory service database.


## -struct-fields




### -field pszAttrName

A  null-terminated Unicode string that contains the name of the attribute whose values are contained in the current search column.


### -field dwADsType

Value from the  <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> enumeration that indicates how the attribute values are interpreted.


### -field pADsValues

Array of  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures that contain values of the attribute in the current search column for the current row.


### -field dwNumValues

Size of the <b>pADsValues</b> array.


### -field hReserved

Reserved for internal use by providers.


## -remarks



The <b>ADS_SEARCH_COLUMN</b> structure only contains a pointer to the array of  <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures. Memory for the structure must be allocated separately.

For more information about  <b>ADS_SEARCH_COLUMN</b>, see  <a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a>



<a href="https://msdn.microsoft.com/3bcacb24-a4b4-4fad-ab7c-79ef7a67064d">IDirectorySearch::GetColumn</a>
 

 

