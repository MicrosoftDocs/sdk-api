---
UID: NE:webservices.WS_MOVE_TO
title: WS_MOVE_TO
author: windows-sdk-content
description: This enumeration identifies the various ways to move about an xml document.
old-location: wsw\ws_move_to.htm
tech.root: wsw
ms.assetid: 9d1623cc-7a88-4a84-ba75-decc4de9fe00
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WS_MOVE_TO, WS_MOVE_TO enumeration [Web Services for Windows], WS_MOVE_TO_BOF, WS_MOVE_TO_CHILD_ELEMENT, WS_MOVE_TO_CHILD_NODE, WS_MOVE_TO_END_ELEMENT, WS_MOVE_TO_EOF, WS_MOVE_TO_FIRST_NODE, WS_MOVE_TO_NEXT_ELEMENT, WS_MOVE_TO_NEXT_NODE, WS_MOVE_TO_PARENT_ELEMENT, WS_MOVE_TO_PREVIOUS_ELEMENT, WS_MOVE_TO_PREVIOUS_NODE, WS_MOVE_TO_ROOT_ELEMENT, webservices/WS_MOVE_TO, webservices/WS_MOVE_TO_BOF, webservices/WS_MOVE_TO_CHILD_ELEMENT, webservices/WS_MOVE_TO_CHILD_NODE, webservices/WS_MOVE_TO_END_ELEMENT, webservices/WS_MOVE_TO_EOF, webservices/WS_MOVE_TO_FIRST_NODE, webservices/WS_MOVE_TO_NEXT_ELEMENT, webservices/WS_MOVE_TO_NEXT_NODE, webservices/WS_MOVE_TO_PARENT_ELEMENT, webservices/WS_MOVE_TO_PREVIOUS_ELEMENT, webservices/WS_MOVE_TO_PREVIOUS_NODE, webservices/WS_MOVE_TO_ROOT_ELEMENT, wsw.ws_move_to
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - WS_MOVE_TO
product: Windows
targetos: Windows
req.typenames: WS_MOVE_TO
req.redist: 
---

# WS_MOVE_TO enumeration


## -description


This enumeration identifies the various ways to move about an xml document.
      


## -enum-fields




### -field WS_MOVE_TO_ROOT_ELEMENT

Moves to the topmost element in the document.  If there is no root element, then the position is left unchanged.
        


### -field WS_MOVE_TO_NEXT_ELEMENT

Moves to the next element with the same depth and parent as the current node.  Text and comments are skipped.  If no element
          is found, then the position is left unchanged.
        


### -field WS_MOVE_TO_PREVIOUS_ELEMENT

Moves to the previous element with the same depth and parent as the current node.  Text and comments are skipped.  If no element
          is found, then the position is left unchanged.
        


### -field WS_MOVE_TO_CHILD_ELEMENT

Moves to the first child element below the current node.  Text and comments are skipped.  If no element is found, then the
          position is left unchanged.
        


### -field WS_MOVE_TO_END_ELEMENT

If the current node is an element, then moves to its corresponding end element.  Otherwise, the position is left
          unchanged.
        


### -field WS_MOVE_TO_PARENT_ELEMENT

Moves to the element node containing the current node.  End elements are considered the last child of their
          corresponding start element.  If the current position is the root element, then the position will be moved
          to <a href="https://msdn.microsoft.com/eddef5db-432d-4615-9f0f-a712dffe42ab">WS_XML_NODE_TYPE_BOF</a>.  If the current position is <b>WS_XML_NODE_TYPE_BOF</b>, then
          current position is left unchanged.
        


### -field WS_MOVE_TO_NEXT_NODE

Moves to the next sibling of the current node.  If the current node is an end element, then the position is left unchanged.
        


### -field WS_MOVE_TO_PREVIOUS_NODE

Moves to the previous sibling of the current node.  If the current node is the first child of an element, then the position
          is left unchanged.
        


### -field WS_MOVE_TO_FIRST_NODE

Moves to the first child of the parent of the current node.
        


### -field WS_MOVE_TO_BOF

Moves to the position logically before the first node in the document.
        


### -field WS_MOVE_TO_EOF

Moves to the position logically after the last node in the document.
        


### -field WS_MOVE_TO_CHILD_NODE

Moves to the first child of the current node.  If the node has no children then the position is left unchanged.
        

