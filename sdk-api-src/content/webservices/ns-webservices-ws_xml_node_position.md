---
UID: NS:webservices._WS_XML_NODE_POSITION
title: WS_XML_NODE_POSITION (webservices.h)
description: Represents a position within an XML buffer.
helpviewer_keywords: ["WS_XML_NODE_POSITION","WS_XML_NODE_POSITION structure [Web Services for Windows]","webservices/WS_XML_NODE_POSITION","wsw.ws_xml_node_position"]
old-location: wsw\ws_xml_node_position.htm
tech.root: wsw
ms.assetid: 40ca058c-04e1-4358-b330-360a094a8791
ms.date: 12/05/2018
ms.keywords: WS_XML_NODE_POSITION, WS_XML_NODE_POSITION structure [Web Services for Windows], webservices/WS_XML_NODE_POSITION, wsw.ws_xml_node_position
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
targetos: Windows
req.typenames: WS_XML_NODE_POSITION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_NODE_POSITION
 - webservices/_WS_XML_NODE_POSITION
 - WS_XML_NODE_POSITION
 - webservices/WS_XML_NODE_POSITION
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
 - WS_XML_NODE_POSITION
---

# WS_XML_NODE_POSITION structure


## -description

Represents a position within an XML buffer.  The current position within
         a reader or writer may be obtained by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a> or
         <a href="/windows/desktop/api/webservices/nf-webservices-wsgetwriterposition">WsGetWriterPosition</a>.  The current position within a reader or writer
        may be set by calling <a href="/windows/desktop/api/webservices/nf-webservices-wssetreaderposition">WsSetReaderPosition</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wssetwriterposition">WsSetWriterPosition</a>.
      

Using <a href="/windows/desktop/api/webservices/nf-webservices-wsremovenode">WsRemoveNode</a> to remove a node that corresponds to or contains a 
        position will cause subsequent use of the position to fail.  The position itself 
        remains valid, but operations that depend on that position will fail.
      

Positions may be used as long as the containing XML buffer is valid.  Using a position 
        after its corresponding buffer has been deleted will exhibit undefined behavior.

## -struct-fields

### -field buffer

The xml buffer to which the position refers.

### -field node

An internal handle to the node.