---
UID: NS:webservices._WS_XML_TEXT
title: "_WS_XML_TEXT"
author: windows-sdk-content
description: Represents a node of text content in xml.
old-location: wsw\ws_xml_text.htm
old-project: wsw
ms.assetid: 430edd13-b664-4e10-8d61-ffa6a01dcb90
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_XML_TEXT, WS_XML_TEXT structure [Web Services for Windows], _WS_XML_TEXT, webservices/WS_XML_TEXT, wsw.ws_xml_text
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_XML_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_TEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_TEXT structure


## -description


Represents a node of text content in xml.
      


## -struct-fields




### -field textType


## -remarks



XML has no concept of typed content; all content is textual in nature.  In some cases this is inefficient, requiring
        translation between text and natural form (e.g. the characters '1','2','8' and the numerical value 128) or requiring
        more bytes of storage for the representation (e.g. the characters '2',5','5' might take 3 bytes, while the numerical
        value 255 could only take 1).
        This structure provides a way to indicate textual content in xml without physically representing it as the characters
        that comprise that value.
      



