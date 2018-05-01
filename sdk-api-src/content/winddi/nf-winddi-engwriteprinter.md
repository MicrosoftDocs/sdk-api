---
UID: NF:winddi.EngWritePrinter
title: EngWritePrinter function
author: windows-driver-content
description: The EngWritePrinter function allows printer graphics DLLs to send a data stream to printer hardware.
old-location: display\engwriteprinter.htm
old-project: display
ms.assetid: c65f09b2-5924-479a-8067-a1ba472348e2
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: EngWritePrinter, EngWritePrinter function [Display Devices], display.engwriteprinter, gdifncs_ec307778-86e1-4f8c-96c8-66c86e196a67.xml, winddi/EngWritePrinter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngWritePrinter
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

