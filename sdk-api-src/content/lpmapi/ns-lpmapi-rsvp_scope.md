---
UID: NS:lpmapi.RSVP_SCOPE
title: RSVP_SCOPE
author: windows-sdk-content
description: The RSVP_SCOPE structure provides RSVP scope information.
old-location: qos\rsvp_scope.htm
tech.root: QOS
ms.assetid: 64a7e461-d767-4571-97ca-cf7862a05d18
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RSVP_SCOPE, RSVP_SCOPE structure [QOS], lpmapi/RSVP_SCOPE, qos.rsvp_scope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - RSVP_SCOPE
product: Windows
targetos: Windows
req.typenames: RSVP_SCOPE
req.redist: 
---

# RSVP_SCOPE structure


## -description


The 
<b>RSVP_SCOPE</b> structure provides RSVP scope information.


## -struct-fields




### -field scopl_header

Scope header, in the form of an <a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a> structure.


### -field scope_u

Union containing scope list information.


### -field scope_u.scopl_ipv4

RSVP scope list, in the form of a <a href="https://msdn.microsoft.com/f1651371-d192-45d9-9a9e-d272b624f40d">Scope_list_ipv4</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/90a237c0-0e62-4f27-927a-e3f3c1ac629e">RsvpObjHdr</a>



<a href="https://msdn.microsoft.com/f1651371-d192-45d9-9a9e-d272b624f40d">Scope_list_ipv4</a>
 

 

