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

# StringDigitSubstitute enumeration


## -description


The <b>StringDigitSubstitute</b> enumeration specifies how to substitute digits in a string according to a user's locale or language.


## -enum-fields




### -field StringDigitSubstituteUser

Specifies a user-defined substitution scheme. 


### -field StringDigitSubstituteNone

Specifies to disable substitutions. 


### -field StringDigitSubstituteNational

Specifies substitution digits that correspond with the official national language of the user's locale. 


### -field StringDigitSubstituteTraditional

Specifies substitution digits that correspond with the user's native script or language, which may be different from the official national language of the user's locale. 

