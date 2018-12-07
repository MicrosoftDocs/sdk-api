---
UID: NS:infocard._POLICY_ELEMENT
title: "_POLICY_ELEMENT"
author: windows-sdk-content
description: The POLICY_ELEMENT structure contains an RSVP policy element.
old-location: qos\policy_element.htm
tech.root: QOS
ms.assetid: 710ed81d-d455-4912-8aee-2f06db894c95
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_ELEMENT, POLICY_ELEMENT, POLICY_ELEMENT structure [QOS], _POLICY_ELEMENT, infocard/POLICY_ELEMENT, qos.policy_element"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: infocard.h
req.include-header: Lpmapi.h
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
 - infocard.h
api_name:
 - POLICY_ELEMENT
product: Windows
targetos: Windows
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
req.redist: 
---

# _POLICY_ELEMENT structure


## -description


The 
<b>POLICY_ELEMENT</b> structure contains an RSVP policy element.


## -struct-fields




### -field targetEndpointAddress

 


### -field issuerEndpointAddress

 


### -field issuedTokenParameters

 


### -field privacyNoticeLink

 


### -field privacyNoticeVersion

 


### -field useManagedPresentation

 




#### - ucPeData

Policy Element data.


#### - usPeLength

Length of the Policy Element, in bytes.


#### - usPeType

Policy Element type.

