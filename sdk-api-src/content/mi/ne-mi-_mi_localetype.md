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

# _MI_LocaleType enumeration


## -description


Type of locale is needed when setting and getting locales.


## -enum-fields




### -field MI_LOCALE_TYPE_REQUESTED_UI

The preferred language of error messages and dialog boxes.


### -field MI_LOCALE_TYPE_REQUESTED_DATA

The preferred date/time formats and  whether a comma or a decimal point is used in a floating-point number.


### -field MI_LOCALE_TYPE_CLOSEST_UI

The fallback error messages language if the requested language is not available.


### -field MI_LOCALE_TYPE_CLOSEST_DATA

The fallback data format if the requested language is not available.

