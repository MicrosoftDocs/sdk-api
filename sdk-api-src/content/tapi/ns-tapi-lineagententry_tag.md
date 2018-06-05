---
UID: NS:tapi.lineagententry_tag
title: lineagententry_tag
author: windows-sdk-content
description: The LINEAGENTENTRY structure describes an individual ACD agent. The LINEAGENTLIST structure can contain an array of LINEAGENTENTRY structures.
old-location: tapi2\lineagententry_str.htm
old-project: Tapi
ms.assetid: 89feff58-3396-4999-be24-4d14839378e1
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINEAGENTENTRY, LINEAGENTENTRY, LINEAGENTENTRY structure [TAPI 2.2], LPLINEAGENTENTRY, LPLINEAGENTENTRY structure pointer [TAPI 2.2], _tapi2_lineagententry_str, lineagententry_tag, tapi/LINEAGENTENTRY, tapi/LPLINEAGENTENTRY, tapi2.lineagententry_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LINEAGENTENTRY, *LPLINEAGENTENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEAGENTENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineagententry_tag structure


## -description


The 
<b>LINEAGENTENTRY</b> structure describes an individual ACD agent. The 
<a href="https://msdn.microsoft.com/176beb90-a9aa-4d40-9f84-e6ea9f84b5a2">LINEAGENTLIST</a> structure can contain an array of 
<b>LINEAGENTENTRY</b> structures.


## -struct-fields




### -field hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field dwNameSize

Size of the agent name string including the <b>null</b> terminator, in bytes. 


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the agent, which is also the operating system's user name. The size of the string is specified by <b>dwNameSize</b>.


### -field dwIDSize

Size of the ID string including the <b>null</b> terminator, in bytes.


### -field dwIDOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the ID of the agent. Used by legacy ACD systems to identify the agent. The size of the string is specified by <b>dwIDSize</b>.


### -field dwPINSize

Size of the PIN string, in bytes.


### -field dwPINOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the PIN or password of the agent. Used by legacy ACD systems for agent authorization. The size of the string is specified by <b>dwPINSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/176beb90-a9aa-4d40-9f84-e6ea9f84b5a2">LINEAGENTLIST</a>
 

 

