---
UID: NS:tapi.lineagentgroupentry_tag
title: lineagentgroupentry_tag
author: windows-driver-content
description: The LINEAGENTGROUPENTRY structure provides information on ACD agent groups. The LINEAGENTGROUPLIST structure can contain an array of LINEAGENTGROUPENTRY structures.
old-location: tapi2\lineagentgroupentry_str.htm
old-project: Tapi
ms.assetid: b1814ef7-7585-4203-8eb2-6862445f9114
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPLINEAGENTGROUPENTRY, LINEAGENTGROUPENTRY, LINEAGENTGROUPENTRY structure [TAPI 2.2], LPLINEAGENTGROUPENTRY, LPLINEAGENTGROUPENTRY structure pointer [TAPI 2.2], _tapi2_lineagentgroupentry_str, lineagentgroupentry_tag, tapi/LINEAGENTGROUPENTRY, tapi/LPLINEAGENTGROUPENTRY, tapi2.lineagentgroupentry_str"
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
req.typenames: LINEAGENTGROUPENTRY, *LPLINEAGENTGROUPENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tapi.h
api_name:
-	LINEAGENTGROUPENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineagentgroupentry_tag structure


## -description


The 
<b>LINEAGENTGROUPENTRY</b> structure provides information on ACD agent groups. The 
<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a> structure can contain an array of 
<b>LINEAGENTGROUPENTRY</b> structures.


## -struct-fields




### -field GroupID



#### dwGroupID1

First part of the universally unique identifier for the group.



#### dwGroupID2

Second part of the universally unique identifier for the group.



#### dwGroupID3

Third part of the universally unique identifier for the group.



#### dwGroupID4

Fourth part of the universally unique identifier for a group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwNameSize

Size of the ACD group or queue name including the <b>null</b> terminator, in bytes.


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string specifying the name and other identifying information of an ACD group or queue into which the agent can log in. This string can contain such information as supervisor and skill level, to assist the agent in selecting the correct group from a list displayed on their workstation screen. The size of the field is specified by <b>dwNameSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6189eb8e-20a4-4c87-bc7f-0a6af9605be7">LINEAGENTGROUPLIST</a>



<a href="https://msdn.microsoft.com/b3767efd-8f7a-4a03-81f6-97e11994900d">lineGetAgentGroupList</a>



<a href="https://msdn.microsoft.com/3e1d63e2-f87d-41ed-92ba-fe3bbdade8d3">lineGetGroupList</a>



<a href="https://msdn.microsoft.com/ce6795fb-fe11-4125-abeb-9b2686ea669a">lineSetAgentGroup</a>
 

 

