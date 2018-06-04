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

# WS_DYNAMIC_STRING_CALLBACK callback function


## -description


Determines whether the specified string can be written in optimized form. This callback is used in <a href="https://msdn.microsoft.com/b4485490-b5e1-406c-883c-a30bfa334316">WS_XML_WRITER_BINARY_ENCODING</a>



## -parameters




### -param *callbackState [in]


          User-defined state that was passed to the function that accepted the <i>WS_DYNAMIC_STRING_CALLBACK</i>.
        


### -param *string [in]


          The string to look up in the dynamic dictionary.
        


### -param *found [out]


          Whether or not the string was found in the dynamic dictionary is returned here.
        


### -param *id [out]


          The id of the string is returned here.
        


### -param *error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



This callback function does not return a value.



