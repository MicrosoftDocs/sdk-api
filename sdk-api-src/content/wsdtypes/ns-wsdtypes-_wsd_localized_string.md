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

# _WSD_LOCALIZED_STRING structure


## -description


Represents a single localized string.


## -struct-fields




### -field lang

The standard language code used for localization. Valid language codes are specified in <a href="Http://go.microsoft.com/fwlink/p/?linkid=84408">RFC 1766</a>.


### -field String

The string data in the localized language.


## -remarks



<a href="Http://go.microsoft.com/fwlink/p/?linkid=84408">RFC 1766</a> extends <a href="Http://go.microsoft.com/fwlink/p/?linkid=84445">ISO-639</a>. Dialect extensions to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=84445">ISO-639</a> codes are used for the <i>lang</i> member. For example, "en-US" is used to indicate a string localized for the USA/English dialect.



