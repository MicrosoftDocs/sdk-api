---
UID: NS:tapi.linecountrylist_tag
title: linecountrylist_tag
author: windows-driver-content
description: The LINECOUNTRYLIST structure describes a list of countries/regions. This structure can contain an array of LINECOUNTRYENTRY structures. LINECOUNTRYLIST is returned by the lineGetCountry function.
old-location: tapi2\linecountrylist_str.htm
old-project: Tapi
ms.assetid: f6634d40-0c17-4eb1-a0ca-9590e9e649e2
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: "*LPLINECOUNTRYLIST, LINECOUNTRYLIST, LINECOUNTRYLIST structure [TAPI 2.2], LPLINECOUNTRYLIST, LPLINECOUNTRYLIST structure pointer [TAPI 2.2], _tapi2_linecountrylist_str, linecountrylist_tag, tapi/LINECOUNTRYLIST, tapi/LPLINECOUNTRYLIST, tapi2.linecountrylist_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: LINECOUNTRYLIST, *LPLINECOUNTRYLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINECOUNTRYLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

