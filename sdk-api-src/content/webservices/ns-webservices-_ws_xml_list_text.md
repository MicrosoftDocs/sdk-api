---
UID: NS:webservices._WS_XML_LIST_TEXT
title: "_WS_XML_LIST_TEXT"
author: windows-driver-content
description: Represents a list of text values separated by a single whitespace character.
old-location: wsw\ws_xml_list_text.htm
old-project: wsw
ms.assetid: a9428114-6f39-46cb-b77f-9da096ed7f11
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_XML_LIST_TEXT, WS_XML_LIST_TEXT structure [Web Services for Windows], _WS_XML_LIST_TEXT, webservices/WS_XML_LIST_TEXT, wsw.ws_xml_list_text
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WS_XML_LIST_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_LIST_TEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_LIST_TEXT structure


## -description



        Represents a list of text values separated by a single whitespace character.
      


        (e.g. The list { { WS_XML_TEXT_TYPE_INT32 }, 123}, 
        { { WS_XML_TEXT_TYPE_BOOL }, 1 } represents the text "123 true")
      


## -struct-fields




### -field text


          The base type for all types that derive from <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a>.
        


### -field itemCount


          The number of items in the list.
        


### -field items


          The list of items.
        

