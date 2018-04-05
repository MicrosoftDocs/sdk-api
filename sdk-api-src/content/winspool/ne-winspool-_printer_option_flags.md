---
UID: NE:winspool._PRINTER_OPTION_FLAGS
title: "_PRINTER_OPTION_FLAGS"
author: windows-driver-content
description: Specifies the caching of a handle for a printer opened with OpenPrinter2.
old-location: gdi\printer_option_flags.htm
old-project: printdocs
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PRINTER_OPTION_CACHE, PRINTER_OPTION_CLIENT_CHANGE, PRINTER_OPTION_FLAGS, PRINTER_OPTION_FLAGS enumeration [Windows GDI], PRINTER_OPTION_NO_CACHE, _PRINTER_OPTION_FLAGS, _win32_PRINTER_OPTION_FLAGS, gdi.printer_option_flags, winspool/PRINTER_OPTION_CACHE, winspool/PRINTER_OPTION_CLIENT_CHANGE, winspool/PRINTER_OPTION_FLAGS, winspool/PRINTER_OPTION_NO_CACHE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_OPTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_OPTION_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_OPTION_FLAGS enumeration


## -description


Specifies the caching of a handle for a printer opened with <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>.


## -enum-fields




### -field PRINTER_OPTION_NO_CACHE

The handle is not cached. All functions applied to a handle returned by <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> will go to the remote computer.


### -field PRINTER_OPTION_CACHE

The handle is cached. All functions applied to a handle returned by <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> will go to the local cache.


### -field PRINTER_OPTION_CLIENT_CHANGE

The handle returned by <a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a> can be used by <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> to rename the printer connection.


### -field PRINTER_OPTION_NO_CLIENT_DATA




## -see-also




<a href="https://msdn.microsoft.com/e2370ae4-4475-4ccc-a6f9-3d33d1370054">OpenPrinter2</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

