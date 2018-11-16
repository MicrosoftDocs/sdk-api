---
UID: NS:dxgi1_2.DXGI_OUTDUPL_POINTER_POSITION
title: DXGI_OUTDUPL_POINTER_POSITION
author: windows-sdk-content
description: The DXGI_OUTDUPL_POINTER_POSITION structure describes the position of the hardware cursor.
old-location: direct3ddxgi\dxgi_outdupl_pointer_position.htm
tech.root: direct3ddxgi
ms.assetid: CCD55021-8F67-463D-BA00-46D8B9D22B9A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DXGI_OUTDUPL_POINTER_POSITION, DXGI_OUTDUPL_POINTER_POSITION structure [DXGI], direct3ddxgi.dxgi_outdupl_pointer_position, dxgi1_2/DXGI_OUTDUPL_POINTER_POSITION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - DXGI1_2.h
api_name:
 - DXGI_OUTDUPL_POINTER_POSITION
product: Windows
targetos: Windows
req.typenames: DXGI_OUTDUPL_POINTER_POSITION
req.redist: 
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
 

 

