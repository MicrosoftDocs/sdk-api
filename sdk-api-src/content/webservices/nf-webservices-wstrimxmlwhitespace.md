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

# WsTrimXmlWhitespace function


## -description



        Removes leading and trailing whitespace from a sequence of characters.
      


## -parameters




### -param chars


          The string to be trimmed.
        


### -param charCount [in]


          The length of the string to be trimmed.
        


### -param trimmedChars


          Returns a pointer into the original string starting at the first non-whitespace character.
        


### -param trimmedCount [out]


          Returns the length of the trimmed string.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The function returns a pointer into the original string.  The original string passed in is not modified.
      


        XML defines whitespace as characters 9 (0x9), 10 (0xA), 13 (0xD), and 32 (0x20).
      



