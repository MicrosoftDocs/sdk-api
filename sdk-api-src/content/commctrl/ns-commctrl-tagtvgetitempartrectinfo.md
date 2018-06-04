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

# tagTVGETITEMPARTRECTINFO structure


## -description


Contains information for identifying the "hit zone" for a specified part of a tree item. The structure is used with the <a href="https://msdn.microsoft.com/4fa5d167-9649-4346-89c2-8a48e8d4d2f6">TVM_GETITEMPARTRECT</a> message and the <a href="https://msdn.microsoft.com/1a0175dc-5ce9-472e-91bc-b58a087b0e77">TreeView_GetItemPartRect</a> macro.


## -struct-fields




### -field hti

Type: <b>HTREEITEM</b>

Handle to the parent item.


### -field prc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure to receive the coordinates of the bounding rectangle. The sender of the message (the caller) is responsible for allocating this structure.


### -field partID

Type: <b>TVITEMPART</b>

ID of the item part. This value must be <b>TVGIPR_BUTTON</b> (0x0001).

