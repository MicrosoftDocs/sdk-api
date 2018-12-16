---
UID: NF:webservices.WsTrimXmlWhitespace
title: WsTrimXmlWhitespace function
author: windows-sdk-content
description: Removes leading and trailing whitespace from a sequence of characters.
old-location: wsw\wstrimxmlwhitespace.htm
tech.root: wsw
ms.assetid: afefbf03-27fc-4e0e-bba2-ce42cf9ab01d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsTrimXmlWhitespace, WsTrimXmlWhitespace function [Web Services for Windows], webservices/WsTrimXmlWhitespace, wsw.wstrimxmlwhitespace
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsTrimXmlWhitespace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
      



