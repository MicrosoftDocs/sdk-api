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

# _MF_CROSS_ORIGIN_POLICY enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Maps to the W3C cross origin settings (CORS) attribute used by the HTML5 media element


## -enum-fields




### -field MF_CROSS_ORIGIN_POLICY_NONE

No CORS state.


### -field MF_CROSS_ORIGIN_POLICY_ANONYMOUS

 Requests for the element will have their mode set to "cors" and their credentials mode set to "same-origin".


### -field MF_CROSS_ORIGIN_POLICY_USE_CREDENTIALS

Requests for the element will have their mode set to "cors" and their credentials mode set to "include".

