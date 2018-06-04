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

# DWRITE_FONT_PROPERTY structure


## -description


Font property used for filtering font sets and
      building a font set with explicit properties.


## -struct-fields




### -field propertyId

Specifies the requested font property, such as DWRITE_FONT_PROPERTY_ID_FAMILY_NAME.


### -field propertyValue

Specifies the value, such as "Segoe UI".


### -field localeName

Specifies the locale to use, such as "en-US". Simply leave this empty when used
          with the font set filtering functions, as they will find a match regardless of
          language. For passing to AddFontFaceReference, the localeName specifies the language
          of the property value.

