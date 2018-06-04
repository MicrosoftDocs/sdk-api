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
        

