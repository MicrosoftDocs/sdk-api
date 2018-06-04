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

# linecountrylist_tag structure


## -description


The 
<b>LINECOUNTRYLIST</b> structure describes a list of countries/regions. This structure can contain an array of 
<a href="https://msdn.microsoft.com/627ff743-f90b-4bcb-b646-cdbc9f768ad2">LINECOUNTRYENTRY</a> structures. 
<b>LINECOUNTRYLIST</b> is returned by the 
<a href="https://msdn.microsoft.com/4de271b3-d93b-4fc9-b853-e26ef1ae75ae">lineGetCountry</a> function.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwNumCountries

Number of 
<a href="https://msdn.microsoft.com/627ff743-f90b-4bcb-b646-cdbc9f768ad2">LINECOUNTRYENTRY</a> structures present in the array defined by <b>dwCountryListSize</b> and <b>dwCountryListOffset</b>.


### -field dwCountryListSize

Size of the array of country/region information, in bytes.


### -field dwCountryListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/627ff743-f90b-4bcb-b646-cdbc9f768ad2">LINECOUNTRYENTRY</a> structures that provides the information for each country/region. The size of the field is specified by <b>dwCountryListSize</b>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/627ff743-f90b-4bcb-b646-cdbc9f768ad2">LINECOUNTRYENTRY</a>



<a href="https://msdn.microsoft.com/4de271b3-d93b-4fc9-b853-e26ef1ae75ae">lineGetCountry</a>
 

 

