---
UID: NS:winspool._PROVIDOR_INFO_1W
title: "_PROVIDOR_INFO_1W"
author: windows-driver-content
description: The PROVIDOR_INFO_1 structure identifies a print provider.
old-location: gdi\providor_info_1.htm
old-project: printdocs
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPROVIDOR_INFO_1W, *PPROVIDOR_INFO_1W, PPROVIDOR_INFO_1, PPROVIDOR_INFO_1 structure pointer [Windows GDI], PROVIDOR_INFO_1, PROVIDOR_INFO_1 structure [Windows GDI], PROVIDOR_INFO_1W, _PROVIDOR_INFO_1A, _PROVIDOR_INFO_1W, _win32_PROVIDOR_INFO_1_str, gdi.providor_info_1, winspool/PPROVIDOR_INFO_1, winspool/PROVIDOR_INFO_1, winspool/_PROVIDOR_INFO_1A, winspool/_PROVIDOR_INFO_1W"
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
req.unicode-ansi: "_PROVIDOR_INFO_1W (Unicode) and _PROVIDOR_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROVIDOR_INFO_1W, *PPROVIDOR_INFO_1W, *LPPROVIDOR_INFO_1W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PROVIDOR_INFO_1
-	_PROVIDOR_INFO_1A
-	_PROVIDOR_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PROVIDOR_INFO_1W structure


## -description



The <b>PROVIDOR_INFO_1</b> structure identifies a print provider.




## -struct-fields




### -field pName

Pointer to a null-terminated string that is the name of the print provider.


### -field pEnvironment

Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.


### -field pDLLName

Pointer to a null-terminated string that is the name of the provider .dll.


## -see-also




<a href="https://msdn.microsoft.com/f34549c3-0474-48ba-9307-5b36f02dbe1c">AddPrintProvidor</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

