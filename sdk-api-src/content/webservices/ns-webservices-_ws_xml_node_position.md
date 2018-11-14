---
UID: NS:webservices._WS_XML_NODE_POSITION
title: "_WS_XML_NODE_POSITION"
author: windows-sdk-content
description: Represents a position within an XML buffer.
old-location: wsw\ws_xml_node_position.htm
tech.root: wsw
ms.assetid: 40ca058c-04e1-4358-b330-360a094a8791
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WS_XML_NODE_POSITION, WS_XML_NODE_POSITION structure [Web Services for Windows], _WS_XML_NODE_POSITION, webservices/WS_XML_NODE_POSITION, wsw.ws_xml_node_position
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WS_XML_NODE_POSITION
product: Windows
targetos: Windows
req.typenames: WS_XML_NODE_POSITION
req.redist: 
---

# _WS_XML_NODE_POSITION structure


## -description


Represents a position within an XML buffer.  The current position within
         a reader or writer may be obtained by calling <a href="https://msdn.microsoft.com/91e543f3-7325-4a90-9b99-c98918478853">WsGetReaderPosition</a> or
         <a href="https://msdn.microsoft.com/0c0fbd78-ed4f-40da-a63d-a2f38136ecb3">WsGetWriterPosition</a>.  The current position within a reader or writer
        may be set by calling <a href="https://msdn.microsoft.com/cc879cc0-c8ca-457e-9ff1-ae220e31cb04">WsSetReaderPosition</a> or <a href="https://msdn.microsoft.com/1d23bda1-d1da-44d4-9a9d-258bba200b29">WsSetWriterPosition</a>.
      

Using <a href="https://msdn.microsoft.com/955fd0b3-b351-40db-a25f-dd1ed8b55550">WsRemoveNode</a> to remove a node that corresponds to or contains a 
        position will cause subsequent use of the position to fail.  The position itself 
        remains valid, but operations that depend on that position will fail.
      

Positions may be used as long as the containing XML buffer is valid.  Using a position 
        after its corresponding buffer has been deleted will exhibit undefined behavior.
      


## -struct-fields




### -field buffer

The xml buffer to which the position refers.
        


### -field node

An internal handle to the node.
        

