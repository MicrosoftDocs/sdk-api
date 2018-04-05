---
UID: NS:tapi.lineagentlist_tag
title: lineagentlist_tag
author: windows-driver-content
description: The LINEAGENTLIST structure describes a list of ACD agents. This structure can contain an array of LINEAGENTENTRY structures.
old-location: tapi2\lineagentlist.htm
old-project: Tapi
ms.assetid: 176beb90-a9aa-4d40-9f84-e6ea9f84b5a2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPLINEAGENTLIST, LINEAGENTLIST, LINEAGENTLIST structure [TAPI 2.2], LPLINEAGENTLIST, LPLINEAGENTLIST structure pointer [TAPI 2.2], _tapi2_lineagentlist, lineagentlist_tag, tapi/LINEAGENTLIST, tapi/LPLINEAGENTLIST, tapi2.lineagentlist"
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
req.typenames: LINEAGENTLIST, *LPLINEAGENTLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEAGENTLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineagentlist_tag structure


## -description


The 
<b>LINEAGENTLIST</b> structure describes a list of ACD agents. This structure can contain an array of 
<a href="https://msdn.microsoft.com/89feff58-3396-4999-be24-4d14839378e1">LINEAGENTENTRY</a> structures.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/89feff58-3396-4999-be24-4d14839378e1">LINEAGENTENTRY</a> structures that appear in the list array. The value is zero if no agents are available.


### -field dwListSize

Size of the agent list array, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/89feff58-3396-4999-be24-4d14839378e1">LINEAGENTENTRY</a> structures that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEAGENTENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/89feff58-3396-4999-be24-4d14839378e1">LINEAGENTENTRY</a>
 

 

