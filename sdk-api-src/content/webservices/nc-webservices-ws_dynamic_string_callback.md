---
UID: NC:webservices.WS_DYNAMIC_STRING_CALLBACK
title: WS_DYNAMIC_STRING_CALLBACK
author: windows-driver-content
description: Determines whether the specified string can be written in optimized form.
old-location: wsw\ws_dynamic_string_callback.htm
old-project: wsw
ms.assetid: c1520c9a-4360-4ac0-89b8-e80385668051
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_DYNAMIC_STRING_CALLBACK, WS_DYNAMIC_STRING_CALLBACK callback function [Web Services for Windows], webservices/WS_DYNAMIC_STRING_CALLBACK, wsw.ws_dynamic_string_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WebServices.h
api_name:
-	WS_DYNAMIC_STRING_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_DYNAMIC_STRING_CALLBACK callback


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



