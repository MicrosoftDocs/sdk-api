---
UID: NS:winspool._PORT_INFO_1A
title: "_PORT_INFO_1A"
author: windows-driver-content
description: The PORT_INFO_1 structure identifies a supported printer port.
old-location: gdi\port_info_1.htm
old-project: printdocs
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPORT_INFO_1A, *PPORT_INFO_1A, PORT_INFO_1, PORT_INFO_1 structure [Windows GDI], PORT_INFO_1A, PPORT_INFO_1, PPORT_INFO_1 structure pointer [Windows GDI], _PORT_INFO_1A, _PORT_INFO_1W, _win32_PORT_INFO_1_str, gdi.port_info_1, winspool/PORT_INFO_1, winspool/PPORT_INFO_1, winspool/_PORT_INFO_1A, winspool/_PORT_INFO_1W"
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
req.unicode-ansi: "_PORT_INFO_1W (Unicode) and _PORT_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PORT_INFO_1A, *PPORT_INFO_1A, *LPPORT_INFO_1A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PORT_INFO_1
-	_PORT_INFO_1A
-	_PORT_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PORT_INFO_1A structure


## -description



The <b>PORT_INFO_1</b> structure identifies a supported printer port.




## -struct-fields




### -field pName

Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

