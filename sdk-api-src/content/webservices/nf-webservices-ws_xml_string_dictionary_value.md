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

# WS_XML_STRING_DICTIONARY_VALUE macro


## -description



        Provides an initializer for a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> structure when there is an associated dictionary ID.
      


## -parameters




### -param S

TBD


### -param D

TBD


### -param I

TBD






## -remarks




        This initializer assumes the string is a static constant string.  It must be encoded in UTF-8.
      


        The following is example usage:
      

<code>WS_XML_STRING myString = WS_XML_STRING_DICTIONARY_VALUE("MyString", myDictionary, 5);</code>



