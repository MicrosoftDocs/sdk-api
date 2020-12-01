---
UID: NS:tapi.lineagentgroupentry_tag
title: LINEAGENTGROUPENTRY (tapi.h)
description: The LINEAGENTGROUPENTRY structure provides information on ACD agent groups. The LINEAGENTGROUPLIST structure can contain an array of LINEAGENTGROUPENTRY structures.
helpviewer_keywords: ["*LPLINEAGENTGROUPENTRY","LINEAGENTGROUPENTRY","LINEAGENTGROUPENTRY structure [TAPI 2.2]","LPLINEAGENTGROUPENTRY","LPLINEAGENTGROUPENTRY structure pointer [TAPI 2.2]","_tapi2_lineagentgroupentry_str","tapi/LINEAGENTGROUPENTRY","tapi/LPLINEAGENTGROUPENTRY","tapi2.lineagentgroupentry_str"]
old-location: tapi2\lineagentgroupentry_str.htm
tech.root: tapi3
ms.assetid: b1814ef7-7585-4203-8eb2-6862445f9114
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTGROUPENTRY, LINEAGENTGROUPENTRY, LINEAGENTGROUPENTRY structure [TAPI 2.2], LPLINEAGENTGROUPENTRY, LPLINEAGENTGROUPENTRY structure pointer [TAPI 2.2], _tapi2_lineagentgroupentry_str, tapi/LINEAGENTGROUPENTRY, tapi/LPLINEAGENTGROUPENTRY, tapi2.lineagentgroupentry_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LINEAGENTGROUPENTRY, *LPLINEAGENTGROUPENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentgroupentry_tag
 - tapi/lineagentgroupentry_tag
 - LPLINEAGENTGROUPENTRY
 - tapi/LPLINEAGENTGROUPENTRY
 - LINEAGENTGROUPENTRY
 - tapi/LINEAGENTGROUPENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTGROUPENTRY
---

# LINEAGENTGROUPENTRY structure


## -description

The 
<b>LINEAGENTGROUPENTRY</b> structure provides information on ACD agent groups. The 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a> structure can contain an array of 
<b>LINEAGENTGROUPENTRY</b> structures.

## -struct-fields

### -field GroupID

### -field GroupID.dwGroupID1

First part of the universally unique identifier for the group.

### -field GroupID.dwGroupID2

Second part of the universally unique identifier for the group.

### -field GroupID.dwGroupID3

Third part of the universally unique identifier for the group.

### -field GroupID.dwGroupID4

Fourth part of the universally unique identifier for a group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.

### -field dwNameSize

Size of the ACD group or queue name including the <b>null</b> terminator, in bytes.

### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string specifying the name and other identifying information of an ACD group or queue into which the agent can log in. This string can contain such information as supervisor and skill level, to assist the agent in selecting the correct group from a list displayed on their workstation screen. The size of the field is specified by <b>dwNameSize</b>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentgrouplist">LINEAGENTGROUPLIST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentgrouplista">lineGetAgentGroupList</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetgrouplista">lineGetGroupList</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentgroup">lineSetAgentGroup</a>