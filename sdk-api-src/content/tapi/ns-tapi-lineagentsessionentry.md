---
UID: NS:tapi.lineagentsession_tag
title: LINEAGENTSESSIONENTRY (tapi.h)
author: windows-sdk-content
description: The LINEAGENTSESSIONENTRY structure describes an ACD agent session. The LINEAGENTSESSIONLIST structure can contain an array of LINEAGENTSESSIONENTRY structures.
old-location: tapi2\lineagentsessionentry_str.htm
tech.root: Tapi
ms.assetid: 406b003a-11a2-445d-a466-a8549e201199
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEAGENTSESSIONENTRY, LINEAGENTSESSIONENTRY, LINEAGENTSESSIONENTRY structure [TAPI 2.2], LPLINEAGENTSESSIONENTRY, LPLINEAGENTSESSIONENTRY structure pointer [TAPI 2.2], _tapi2_lineagentsessionentry_str, tapi/LINEAGENTSESSIONENTRY, tapi/LPLINEAGENTSESSIONENTRY, tapi2.lineagentsessionentry_str"
ms.topic: struct
f1_keywords: 
 - "tapi/LINEAGENTSESSIONENTRY"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAGENTSESSIONENTRY
product: Windows
targetos: Windows
req.typenames: LINEAGENTSESSIONENTRY, *LPLINEAGENTSESSIONENTRY
req.redist: 
ms.custom: 19H1
---

# LINEAGENTSESSIONENTRY structure


## -description


The 
<b>LINEAGENTSESSIONENTRY</b> structure describes an ACD agent session. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist_tag">LINEAGENTSESSIONLIST</a> structure can contain an array of 
<b>LINEAGENTSESSIONENTRY</b> structures.


## -struct-fields




### -field hAgentSession

Unique identifier for an agent session. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field hAgent

Unique identifier for an agent. It is the responsibility of the agent handler to generate and maintain uniqueness of these identifiers.


### -field GroupID

Universally unique identifier for an ACD group. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwWorkingAddressID

Address identifier on which the agent will receive calls for this session.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-lineagentsessionlist_tag">LINEAGENTSESSIONLIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentsessionlist">lineGetAgentSessionList</a>
 

 

