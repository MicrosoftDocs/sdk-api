---
UID: NF:vfw.ICGetState
title: ICGetState macro
author: windows-sdk-content
description: The ICGetState macro queries a video compression driver to return its current configuration in a block of memory. You can use this macro or explicitly call the ICM_GETSTATE message.
old-location: multimedia\icgetstate.htm
tech.root: Multimedia
ms.assetid: e0066cc2-a67d-4cf4-9d22-506cc152ec14
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICGetState, ICGetState macro [Windows Multimedia], _win32_ICGetState, multimedia.icgetstate, vfw/ICGetState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Vfw.h
api_name:
 - ICGetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICGetState macro


## -description



The <b>ICGetState</b> macro queries a video compression driver to return its current configuration in a block of memory. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4b77e294-f3aa-45f9-a4f4-f103b83eae8d">ICM_GETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param pv

Pointer to a block of memory to contain the current configuration information. You can specify <b>NULL</b> for this parameter to determine the amount of memory required for the configuration information, as in <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a>. 


### -param cb

Size, in bytes, of the block of memory. 


## -remarks



The <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a> macro returns the number of bytes used by the state data.

The structure used to represent configuration information is driver specific and is defined by the driver.

Use <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a> before calling the <b>ICGetState</b> macro to determine the size of buffer to allocate for the call.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

