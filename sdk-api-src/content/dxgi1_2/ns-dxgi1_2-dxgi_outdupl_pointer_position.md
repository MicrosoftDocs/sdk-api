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

# DXGI_OUTDUPL_POINTER_POSITION structure


## -description


The <b>DXGI_OUTDUPL_POINTER_POSITION</b> structure describes the position of the hardware cursor.


## -struct-fields




### -field Position

The position of the hardware cursor relative to the top-left of the adapter output.


### -field Visible

Specifies whether the hardware cursor is visible. <b>TRUE</b> if visible; otherwise, <b>FALSE</b>. If the hardware cursor is not visible, the calling application does not display the cursor in the client.


## -remarks



The <b>Position</b> member is valid only if the <b>Visible</b> member’s value is set to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/2A5C6F99-0610-457D-9850-867DCDA8F293">DXGI_OUTDUPL_FRAME_INFO</a>
 

 

