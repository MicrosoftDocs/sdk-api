---
UID: NS:tapi.linecalllist_tag
title: linecalllist_tag
author: windows-driver-content
description: The LINECALLLIST structure describes a list of call handles. A structure of this type is returned by the lineGetNewCalls and lineGetConfRelatedCalls functions.
old-location: tapi2\linecalllist_str.htm
old-project: Tapi
ms.assetid: b715dd07-74bd-4267-91fe-cfc0cd1e6aa4
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*LPLINECALLLIST, LINECALLLIST, LINECALLLIST structure [TAPI 2.2], LPLINECALLLIST, LPLINECALLLIST structure pointer [TAPI 2.2], _tapi2_linecalllist_str, linecalllist_tag, tapi/LINECALLLIST, tapi/LPLINECALLLIST, tapi2.linecalllist_str"
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
req.typenames: LINECALLLIST, *LPLINECALLLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINECALLLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# linecalllist_tag structure


## -description


The 
<b>LINECALLLIST</b> structure describes a list of call handles. A structure of this type is returned by the 
<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a> and 
<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a> functions.


## -struct-fields




### -field dwTotalSize

Total size allocated to this data structure, in bytes.


### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.


### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.


### -field dwCallsNumEntries

Number of handles in the <i>hCalls</i> array.


### -field dwCallsSize

Size of the array of call handles, in bytes.


### -field dwCallsOffset

Offset from the beginning of the structure to the variably sized array of <b>HCALL</b> handles. The size of the array is specified by <b>dwCallsSize</b>.


## -remarks



This structure may not be extended.




## -see-also




<a href="https://msdn.microsoft.com/048bc4bc-511a-4666-a2ff-4fff5132ed2e">lineGetConfRelatedCalls</a>



<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a>
 

 

