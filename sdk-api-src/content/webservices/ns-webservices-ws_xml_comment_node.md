---
UID: NS:webservices._WS_XML_COMMENT_NODE
title: WS_XML_COMMENT_NODE (webservices.h)
description: Represents a comment.
helpviewer_keywords: ["WS_XML_COMMENT_NODE","WS_XML_COMMENT_NODE structure [Web Services for Windows]","webservices/WS_XML_COMMENT_NODE","wsw.ws_xml_comment_node"]
old-location: wsw\ws_xml_comment_node.htm
tech.root: wsw
ms.assetid: e1a0b493-4537-465b-93bb-64672bc5b3d9
ms.date: 12/05/2018
ms.keywords: WS_XML_COMMENT_NODE, WS_XML_COMMENT_NODE structure [Web Services for Windows], webservices/WS_XML_COMMENT_NODE, wsw.ws_xml_comment_node
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
targetos: Windows
req.typenames: WS_XML_COMMENT_NODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_COMMENT_NODE
 - webservices/_WS_XML_COMMENT_NODE
 - WS_XML_COMMENT_NODE
 - webservices/WS_XML_COMMENT_NODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_COMMENT_NODE
---

# WS_XML_COMMENT_NODE structure


## -description

Represents a comment.  (For example, &lt;!--The message follows--&gt;)

## -struct-fields

### -field node

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">WS_XML_NODE</a>.

### -field value

The textual content of the comment.  In the example, it is the string "The message follows".