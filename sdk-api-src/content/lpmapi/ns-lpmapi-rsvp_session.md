---
UID: NS:lpmapi.__unnamed_struct_2
title: RSVP_SESSION (lpmapi.h)
author: windows-sdk-content
description: The RSVP_SESSION structure stores information about an RSVP SESSION message.
old-location: qos\rsvp_session.htm
tech.root: QOS
ms.assetid: d6674de9-7d79-40f2-ae45-4410408ba047
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RSVP_SESSION, RSVP_SESSION structure [QOS], lpmapi/RSVP_SESSION, qos.rsvp_session
ms.topic: struct
f1_keywords: 
 - "lpmapi/RSVP_SESSION"
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Lpmapi.h
api_name:
 - RSVP_SESSION
targetos: Windows
req.typenames: RSVP_SESSION
req.redist: 
ms.custom: 19H1
---

# RSVP_SESSION structure


## -description


The 
<b>RSVP_SESSION</b> structure stores information about an RSVP SESSION message.


## -struct-fields




### -field sess_header

RSVP Object Header, in the form of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.


### -field sess_u



#### sess_ipv4

Session information, in the form of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-session_ipv4">Session_IPv4</a> structure.


### -field sess_ipv4

 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-session_ipv4">Session_IPv4</a>
 

 

