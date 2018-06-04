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
        

