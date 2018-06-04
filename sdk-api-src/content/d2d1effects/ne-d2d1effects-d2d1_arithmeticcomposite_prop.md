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

# D2D1_ARITHMETICCOMPOSITE_PROP enumeration


## -description



          Identifiers for the properties of the <a href="https://msdn.microsoft.com/6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0">Arithmetic composite effect</a>.
        


## -enum-fields




### -field D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS


            The coefficients for the equation used to composite the two input images. The coefficients are unitless and unbounded.
            

Type is D2D1_VECTOR_4F.

Default value is {1.0f, 0.0f, 0.0f, 0.0f}.


### -field D2D1_ARITHMETICCOMPOSITE_PROP_CLAMP_OUTPUT


            The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
            but other effects and the output surface may clamp the values if they are not of high enough precision.
            

Type is BOOL.

Default value is FALSE.


### -field D2D1_ARITHMETICCOMPOSITE_PROP_FORCE_DWORD



