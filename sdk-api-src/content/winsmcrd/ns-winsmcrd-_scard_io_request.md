---
UID: NS:winsmcrd._SCARD_IO_REQUEST
title: "_SCARD_IO_REQUEST"
author: windows-driver-content
description: The SCARD_IO_REQUEST structure begins a protocol control information structure.
old-location: security\scard_io_request.htm
old-project: SecAuthN
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*LPSCARD_IO_REQUEST, *PSCARD_IO_REQUEST, SCARD_IO_REQUEST, SCARD_IO_REQUEST structure [Security], _SCARD_IO_REQUEST, _smart_scard_io_request, security.scard_io_request, winsmcrd/SCARD_IO_REQUEST"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsmcrd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SCARD_IO_REQUEST, *PSCARD_IO_REQUEST, *LPSCARD_IO_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winsmcrd.h
api_name:
-	SCARD_IO_REQUEST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SCARD_IO_REQUEST structure


## -description


The <b>SCARD_IO_REQUEST</b> structure begins a protocol control information structure. Any protocol-specific information then immediately follows this structure. The entire length of the structure must be aligned with the underlying hardware architecture word size. For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.


## -struct-fields




### -field dwProtocol

Protocol in use.


### -field cbPciLength

Length, in bytes, of the <b>SCARD_IO_REQUEST</b> structure plus any following PCI-specific information.


## -see-also




<a href="https://msdn.microsoft.com/d0c16b67-34e7-4872-aa36-79dcad19093e">SCardTransmit</a>
 

 

