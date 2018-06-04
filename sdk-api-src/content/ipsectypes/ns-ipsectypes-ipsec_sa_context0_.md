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

# IPSEC_SA_CONTEXT0_ structure


## -description


The <b>IPSEC_SA_CONTEXT0</b> structure encapsulates an inbound and outbound SA pair.
<div class="alert"><b>Note</b>  <b>IPSEC_SA_CONTEXT0</b> is the specific implementation of IPSEC_SA_CONTEXT used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/a3e210a7-cd3a-42fc-b3a0-7df9ad6778af">IPSEC_SA_CONTEXT1</a> is available.</div><div> </div>

## -struct-fields




### -field saContextId

Identifies the SA context.


### -field inboundSa

An <a href="https://msdn.microsoft.com/261cea6e-4a56-404f-9e5d-70ce95122f9f">IPSEC_SA_DETAILS0</a> structure that contains information about the inbound SA.


### -field outboundSa

An <a href="https://msdn.microsoft.com/261cea6e-4a56-404f-9e5d-70ce95122f9f">IPSEC_SA_DETAILS0</a> structure that contains information about the outbound SA.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

