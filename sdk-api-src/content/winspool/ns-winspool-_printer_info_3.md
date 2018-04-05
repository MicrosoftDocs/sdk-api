---
UID: NS:winspool._PRINTER_INFO_3
title: "_PRINTER_INFO_3"
author: windows-driver-content
description: The PRINTER_INFO_3 structure specifies printer security information.
old-location: gdi\printer_info_3.htm
old-project: printdocs
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_3, *PPRINTER_INFO_3, PPRINTER_INFO_3, PPRINTER_INFO_3 structure pointer [Windows GDI], PRINTER_INFO_3, PRINTER_INFO_3 structure [Windows GDI], _PRINTER_INFO_3, _win32_PRINTER_INFO_3_str, gdi.printer_info_3, winspool/PPRINTER_INFO_3, winspool/PRINTER_INFO_3"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_3, *PPRINTER_INFO_3, *LPPRINTER_INFO_3
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_3 structure


## -description



The <b>PRINTER_INFO_3</b> structure specifies printer security information.




## -struct-fields




### -field pSecurityDescriptor

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that specifies a printer's security information.


## -remarks



The <b>PRINTER_INFO_3</b> structure lets an application get and set a printer's security descriptor. The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in <a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a> and <a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>. Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.




## -see-also




<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/81bd0eab-dc1e-4cf1-8f63-3686f1711c1f">PRINTER_INFO_4</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/ade367c5-20d6-4da9-bb52-ce6768cf7537">SetPrinter</a>
 

 

