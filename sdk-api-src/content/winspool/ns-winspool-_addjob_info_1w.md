---
UID: NS:winspool._ADDJOB_INFO_1W
title: "_ADDJOB_INFO_1W"
author: windows-driver-content
description: The ADDJOB_INFO_1 structure identifies a print job as well as the directory and file in which an application can store that job.
old-location: gdi\addjob_info_1.htm
old-project: printdocs
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPADDJOB_INFO_1W, *PADDJOB_INFO_1W, ADDJOB_INFO_1, ADDJOB_INFO_1 structure [Windows GDI], ADDJOB_INFO_1W, PADDJOB_INFO_1, PADDJOB_INFO_1 structure pointer [Windows GDI], _ADDJOB_INFO_1A, _ADDJOB_INFO_1W, _JOB_INFO_1A, _JOB_INFO_1W, _win32_ADDJOB_INFO_1_str, gdi.addjob_info_1, winspool/ADDJOB_INFO_1, winspool/PADDJOB_INFO_1, winspool/_ADDJOB_INFO_1A, winspool/_ADDJOB_INFO_1W"
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
req.unicode-ansi: "_ADDJOB_INFO_1W (Unicode) and _ADDJOB_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADDJOB_INFO_1W, *PADDJOB_INFO_1W, *LPADDJOB_INFO_1W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	ADDJOB_INFO_1
-	_ADDJOB_INFO_1A
-	_ADDJOB_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ADDJOB_INFO_1W structure


## -description



The <b>ADDJOB_INFO_1</b> structure identifies a print job as well as the directory and file in which an application can store that job.




## -struct-fields




### -field Path

Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.


### -field JobId

A handle to the print job.


## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

