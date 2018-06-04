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

# WS_XML_TEXT_TYPE enumeration


## -description



        The type of <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a> structure.
      


## -enum-fields




### -field WS_XML_TEXT_TYPE_UTF8

Characters encoded as UTF-8 bytes.
        


### -field WS_XML_TEXT_TYPE_UTF16


          Characters encoded as UTF-16 bytes.
        


### -field WS_XML_TEXT_TYPE_BASE64

Bytes that represent base64 encoded text.
        


### -field WS_XML_TEXT_TYPE_BOOL

A Boolean value that represents the text "true" or "false"
        


### -field WS_XML_TEXT_TYPE_INT32

A signed 32 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_INT64

A signed 64 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_UINT64

An unsigned 64 bit integer value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_FLOAT


          An 4 byte floating point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_DOUBLE


          An 8 byte floating point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_DECIMAL


          A 12 byte fixed point value that represents the text of the value as base 10 characters.
        


### -field WS_XML_TEXT_TYPE_GUID


          A GUID that represents the text "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx".
        


### -field WS_XML_TEXT_TYPE_UNIQUE_ID


          A GUID that represents the text "urn:uuid:xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx".
        


### -field WS_XML_TEXT_TYPE_DATETIME


          A datetime.
        


### -field WS_XML_TEXT_TYPE_TIMESPAN


          A timespan.
        


### -field WS_XML_TEXT_TYPE_QNAME


          A qualified name.
        


### -field WS_XML_TEXT_TYPE_LIST


          A list of values that represent their text forms separated by a single whitespace character.
        

