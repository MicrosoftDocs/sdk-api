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

# D2D1_EMBOSS_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/74f63875-35cd-f335-62cd-410a953e53ea">Emboss effect</a>.


## -enum-fields




### -field D2D1_EMBOSS_PROP_HEIGHT

The D2D1_EMBOSS_PROP_HEIGHT property is a float value controlling the strength of the embossing effect.  The allowed range is 0.0 to 10.0.  The default value is 1.0.


### -field D2D1_EMBOSS_PROP_DIRECTION

The D2D1_EMBOSS_PROP_DIRECTION property is a float value specifying the light direction used to create the effect. The allowed range is 0.0 to 360.0.  The default value is 0.0. 


### -field D2D1_EMBOSS_PROP_FORCE_DWORD



