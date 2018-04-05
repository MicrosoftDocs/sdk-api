---
UID: NS:winspool._PROVIDOR_INFO_2W
title: "_PROVIDOR_INFO_2W"
author: windows-driver-content
description: The PROVIDOR_INFO_2 structure appends a print provider to the print provider order list.
old-location: gdi\providor_info_2.htm
old-project: printdocs
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPROVIDOR_INFO_2W, *PPROVIDOR_INFO_2W, PPROVIDOR_INFO_2, PPROVIDOR_INFO_2 structure pointer [Windows GDI], PROVIDOR_INFO_2, PROVIDOR_INFO_2 structure [Windows GDI], PROVIDOR_INFO_2W, _PROVIDOR_INFO_2A, _PROVIDOR_INFO_2W, _win32_PROVIDOR_INFO_2_str, gdi.providor_info_2, winspool/PPROVIDOR_INFO_2, winspool/PROVIDOR_INFO_2, winspool/_PROVIDOR_INFO_2A, winspool/_PROVIDOR_INFO_2W"
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
req.unicode-ansi: "_PROVIDOR_INFO_2W (Unicode) and _PROVIDOR_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROVIDOR_INFO_2W, *PPROVIDOR_INFO_2W, *LPPROVIDOR_INFO_2W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PROVIDOR_INFO_2
-	_PROVIDOR_INFO_2A
-	_PROVIDOR_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PROVIDOR_INFO_2W structure


## -description



The <b>PROVIDOR_INFO_2</b> structure appends a print provider to the print provider order list.




## -struct-fields




### -field pOrder

Pointer to a null-terminated string that specifies the name of the print provider.


## -remarks



This structure is used when calling <a href="https://msdn.microsoft.com/f34549c3-0474-48ba-9307-5b36f02dbe1c">AddPrintProvidor</a>, level 2, to add the specified print provider to the end of the print provider order list. The provider is immediately used for routing if the call succeeds.




## -see-also




<a href="https://msdn.microsoft.com/f34549c3-0474-48ba-9307-5b36f02dbe1c">AddPrintProvidor</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

