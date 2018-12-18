---
UID: NF:webservices.WS_STRING_VALUE
title: WS_STRING_VALUE macro
author: windows-sdk-content
description: Initializes a WS_STRING structure given a constant string.
old-location: wsw\ws_string_value.htm
tech.root: wsw
ms.assetid: 692aa04e-f061-465c-b2ae-27d424d708bc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_STRING_VALUE, WS_STRING_VALUE macro [Web Services for Windows], webservices/WS_STRING_VALUE, wsw.ws_string_value
ms.topic: macro
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_STRING_VALUE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WS_STRING_VALUE macro


## -description


Initializes a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a> structure given a constant string.
            


## -parameters




### -param S

TBD






## -remarks



The initializer string is assumed to be zero terminated.
            


#### Examples

The following is an example of how to use the macro.
            

<code>WS_STRING myString = WS_STRING_VALUE(L"MyString");</code>

<div class="code"></div>


