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

# EngWritePrinter function


## -description


The <b>EngWritePrinter</b> function allows printer graphics DLLs to send a data stream to printer hardware.


## -parameters




### -param hPrinter [in]

Caller-supplied handle to the printer. This should be the handle received as the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> function's <i>hDriver</i> parameter value.


### -param pBuf [in]

Caller-supplied pointer to a buffer containing a byte stream to be sent to the printer.


### -param cbBuf [in]

Specifies the caller-supplied number of bytes contained in the buffer pointed to by <i>pBuf</i>.


### -param pcWritten [out]

Caller-supplied pointer to a DWORD location that receives the number of bytes actually written to the printer.


## -returns



If the operation succeeds, the function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks




<a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">Printer graphics DLLs</a> call <b>EngWritePrinter</b> to send data streams (either control sequences or image data) to the print spooler, which in turn sends the data to the printer hardware by calling the appropriate <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">print monitor</a>. The function returns after the spooler receives the data.

The buffer pointed to by <i>pBuf</i> cannot be in user memory; that is, <i>pBuf</i> cannot point to memory allocated by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a> with the BMF_USERMEM flag set or by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>.

For additional information about calling <b>EngWritePrinter</b>, see <a href="https://msdn.microsoft.com/78967839-b518-41c0-8825-b00f8b8560e6">Rendering a Print Job</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a>
 

 

