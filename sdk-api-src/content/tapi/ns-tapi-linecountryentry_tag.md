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

# linecountryentry_tag structure


## -description


The 
<b>LINECOUNTRYENTRY</b> structure provides the data for a single country/region entry. An array of one or more of these structures is part of the 
<a href="https://msdn.microsoft.com/f6634d40-0c17-4eb1-a0ca-9590e9e649e2">LINECOUNTRYLIST</a> structure returned by the 
<a href="https://msdn.microsoft.com/4de271b3-d93b-4fc9-b853-e26ef1ae75ae">lineGetCountry</a> function.


## -struct-fields




### -field dwCountryID

Country/region identifier of the entry. The country/region identifier is an internal identifier that allows multiple entries to exist in the country/region list with the same country/region code, for example, all countries or regions in North America and the Caribbean share the country/region code 1, but require separate entries in the list.


### -field dwCountryCode

Country/region code of the country/region represented by the entry; that is, the digits dialed in an international call. Only this value should be displayed to users. Country/region identifiers should never be displayed.


### -field dwNextCountryID

Country/region identifier of the next entry in the country/region list. Because country/region codes and identifiers are not assigned in any regular numeric sequence, the country/region list is a single linked list, with each entry pointing to the next. The last country/region in the list has a <b>dwNextCountryID</b> value of zero. When the 
<a href="https://msdn.microsoft.com/f6634d40-0c17-4eb1-a0ca-9590e9e649e2">LINECOUNTRYLIST</a> structure is used to obtain the entire list, the entries in the list are in sequence as linked by their <b>dwNextCountryID</b> members.


### -field dwCountryNameSize

Size, in bytes, of the name of the country/region including the <b>null</b> terminator.


### -field dwCountryNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the country/region. The size of the field is specified by <b>dwCountryNameSize</b>.


### -field dwSameAreaRuleSize

Size, in bytes, of the direct-dialed dialing rule including the <b>null</b> terminator.


### -field dwSameAreaRuleOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to the same area code. The size of the field is specified by <b>dwSameAreaRuleSize</b>.


### -field dwLongDistanceRuleSize

Size, in bytes, of the long-distance dialing rule including the <b>null</b> terminator.


### -field dwLongDistanceRuleOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to other areas in the same country/region. The size of the field is specified by <b>dwLongDistanceRuleSize</b>.


### -field dwInternationalRuleSize

Size, in bytes, of the international dialing rule including the <b>null</b> terminator.


### -field dwInternationalRuleOffset

Offset from the beginning of the 
<a href="https://msdn.microsoft.com/f6634d40-0c17-4eb1-a0ca-9590e9e649e2">LINECOUNTRYLIST</a> structure to a <b>null</b>-terminated string that contains the dialing rule for direct-dialed calls to other countries/regions. The size of the field is specified by <b>dwInternationalRuleSize</b>.


## -remarks



This structure cannot be extended.




## -see-also




<a href="https://msdn.microsoft.com/f6634d40-0c17-4eb1-a0ca-9590e9e649e2">LINECOUNTRYLIST</a>



<a href="https://msdn.microsoft.com/4de271b3-d93b-4fc9-b853-e26ef1ae75ae">lineGetCountry</a>
 

 

