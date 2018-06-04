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

# D2D1_POSTERIZE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/e6686998-1246-b3b7-6f4f-212568c3191c">Posterize effect</a>.


## -enum-fields




### -field D2D1_POSTERIZE_PROP_RED_VALUE_COUNT

The D2D1_POSTERIZE_PROP_RED_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the red channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.


### -field D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT

The D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the green channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.


### -field D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT

The D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT property is an integer value specifying how many evenly spaced steps to divide the blue channel range of 0.0 to 1.0 into.  
          For example, a value of 4 generates a table with 4 steps, [0.0, 0.33, 0.67, 1.0].  The allowed range for this property is 2 to 16.  The default value is 4.


### -field D2D1_POSTERIZE_PROP_FORCE_DWORD



