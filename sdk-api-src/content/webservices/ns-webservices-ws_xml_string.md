---
UID: NS:webservices._WS_XML_STRING
title: WS_XML_STRING
author: windows-sdk-content
description: Represents a string that optionally has dictionary information associated with it. The xml APIs use WS_XML_STRINGs to identify prefixes, localNames and namespaces.
old-location: wsw\ws_xml_string.htm
tech.root: wsw
ms.assetid: 3daa656f-7f97-4e29-a556-7ff72206f01c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_XML_STRING, WS_XML_STRING structure [Web Services for Windows], webservices/WS_XML_STRING, wsw.ws_xml_string
ms.topic: struct
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
 - WS_XML_STRING
product: Windows
targetos: Windows
req.typenames: WS_XML_STRING
req.redist: 
---

# WS_XML_STRING structure


## -description


Represents a string that optionally has <a href="https://msdn.microsoft.com/2cba47fd-a049-4e50-99dd-20ccf91c9e0f">dictionary</a> 
        information associated with it.  The xml APIs use WS_XML_STRINGs to identify prefixes, 
        localNames and namespaces.
      


## -struct-fields




### -field length

The number of bytes in the UTF-8 encoded representation of the string.
        


### -field bytes

The string encoded as UTF-8 bytes.
        


### -field dictionary

A pointer to the dictionary that contains the string.  If the string is not part of a dictionary
          then the value may be <b>NULL</b>.
        


### -field id

A value that uniquely identifies the string within the specified dictionary.
          The entry at dictionary-&gt;strings[id] should identify this string.
        

If the dictionary is <b>NULL</b>, then this value is unused.
        


## -remarks



The string is represented as UTF-8 encoded bytes, not WCHARs.  It is not required to be zero terminated.
      

The macros <a href="https://msdn.microsoft.com/95e2326c-d4b2-421c-b991-ca9c332b6f6f">WS_XML_STRING_VALUE</a>, <a href="https://msdn.microsoft.com/3a5abf34-16f6-4cac-a5da-35045de4438b">WS_XML_STRING_NULL</a>  and
        <a href="https://msdn.microsoft.com/1e2045c0-11c5-4369-9b82-dc759eb1412e">WS_XML_STRING_DICTIONARY_VALUE</a> can be used to initialize this structure.
      

The dictionary information is used by the binary encoding to write a more compact xml document.
      



