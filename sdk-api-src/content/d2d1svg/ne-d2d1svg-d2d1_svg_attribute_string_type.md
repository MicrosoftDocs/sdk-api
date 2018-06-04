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

# D2D1_SVG_ATTRIBUTE_STRING_TYPE enumeration


## -description


Defines the type of SVG string attribute to set or get.


## -enum-fields




### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG

The attribute is a string in the same form as it would appear in the SVG XML.
          Note that when getting values of this type, the value returned may not exactly match the value that was set. Instead, the output value is a normalized version
          of the value. For example, an input color of 'red' may be output as '#FF0000'.


### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID

The attribute is an element ID.


### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD

