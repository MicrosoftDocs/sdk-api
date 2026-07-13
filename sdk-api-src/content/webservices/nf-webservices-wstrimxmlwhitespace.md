---
UID: NF:webservices.WsTrimXmlWhitespace
title: WsTrimXmlWhitespace function (webservices.h)
description: Removes leading and trailing whitespace from a sequence of characters.
helpviewer_keywords: ["WsTrimXmlWhitespace","WsTrimXmlWhitespace function [Web Services for Windows]","webservices/WsTrimXmlWhitespace","wsw.wstrimxmlwhitespace"]
old-location: wsw\wstrimxmlwhitespace.htm
tech.root: wsw
ms.assetid: afefbf03-27fc-4e0e-bba2-ce42cf9ab01d
ms.date: 12/05/2018
ms.keywords: WsTrimXmlWhitespace, WsTrimXmlWhitespace function [Web Services for Windows], webservices/WsTrimXmlWhitespace, wsw.wstrimxmlwhitespace
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsTrimXmlWhitespace
 - webservices/WsTrimXmlWhitespace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsTrimXmlWhitespace
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function returns a pointer into the original string.  The original string passed in is not modified.
      

XML defines whitespace as characters 9 (0x9), 10 (0xA), 13 (0xD), and 32 (0x20).

