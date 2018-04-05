---
UID: NS:winspool._PRINTPROCESSOR_INFO_1A
title: "_PRINTPROCESSOR_INFO_1A"
author: windows-driver-content
description: The PRINTPROCESSOR_INFO_1 structure specifies the name of an installed print processor.
old-location: gdi\printprocessor_info_1.htm
old-project: printdocs
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTPROCESSOR_INFO_1A, *PPRINTPROCESSOR_INFO_1A, PPRINTPROCESSOR_INFO_1, PPRINTPROCESSOR_INFO_1 structure pointer [Windows GDI], PRINTPROCESSOR_INFO_1, PRINTPROCESSOR_INFO_1 structure [Windows GDI], PRINTPROCESSOR_INFO_1A, _PRINTPROCESSOR_INFO_1A, _PRINTPROCESSOR_INFO_1W, _win32_PRINTPROCESSOR_INFO_1_str, gdi.printprocessor_info_1, winspool/PPRINTPROCESSOR_INFO_1, winspool/PRINTPROCESSOR_INFO_1, winspool/_PRINTPROCESSOR_INFO_1A, winspool/_PRINTPROCESSOR_INFO_1W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_PRINTPROCESSOR_INFO_1W (Unicode) and _PRINTPROCESSOR_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTPROCESSOR_INFO_1A, *PPRINTPROCESSOR_INFO_1A, *LPPRINTPROCESSOR_INFO_1A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTPROCESSOR_INFO_1
-	_PRINTPROCESSOR_INFO_1A
-	_PRINTPROCESSOR_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTPROCESSOR_INFO_1A structure


## -description



The <b>PRINTPROCESSOR_INFO_1</b> structure specifies the name of an installed print processor.




## -struct-fields




### -field pName

Pointer to a null-terminated string that specifies the name of an installed print processor.


## -see-also




<a href="https://msdn.microsoft.com/98c9185c-c89d-4b4e-8c1e-7e22b315f188">EnumPrintProcessors</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

