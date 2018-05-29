---
UID: NF:webservices.WS_XML_STRING_DICTIONARY_VALUE
title: WS_XML_STRING_DICTIONARY_VALUE macro
author: windows-sdk-content
description: Provides an initializer for a WS_XML_STRING structure when there is an associated dictionary ID.
old-location: wsw\ws_xml_string_dictionary_value.htm
old-project: wsw
ms.assetid: 1e2045c0-11c5-4369-9b82-dc759eb1412e
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_XML_STRING_DICTIONARY_VALUE, WS_XML_STRING_DICTIONARY_VALUE function [Web Services for Windows], webservices/WS_XML_STRING_DICTIONARY_VALUE, wsw.ws_xml_string_dictionary_value
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_STRING_DICTIONARY_VALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



