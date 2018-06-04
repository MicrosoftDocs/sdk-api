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

# IPSEC_SA_IDLE_TIMEOUT0_ structure


## -description


The <b>IPSEC_SA_IDLE_TIMEOUT0</b> structure specifies the security association (SA) idle timeout in IPsec policy.


## -struct-fields




### -field idleTimeoutSeconds

Specifies the amount of time in seconds after which IPsec SAs should become  idle.


### -field idleTimeoutSecondsFailOver

Specifies the amount of time in seconds after which IPsec SAs should become idle if the peer machine supports fail over.


## -remarks



<b>IPSEC_SA_IDLE_TIMEOUT0</b> is a specific implementation of IPSEC_SA_IDLE_TIMEOUT. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



