---
UID: NS:winspool._DOC_INFO_1W
title: "_DOC_INFO_1W"
author: windows-driver-content
description: The DOC_INFO_1 structure describes a document that will be printed.
old-location: gdi\doc_info_1.htm
old-project: printdocs
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDOC_INFO_1W, *PDOC_INFO_1W, DOC_INFO_1, DOC_INFO_1 structure [Windows GDI], DOC_INFO_1W, _DOC_INFO_1A, _DOC_INFO_1W, _win32_DOC_INFO_1_str, gdi.doc_info_1, winspool/DOC_INFO_1, winspool/_DOC_INFO_1A, winspool/_DOC_INFO_1W"
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
req.unicode-ansi: "_DOC_INFO_1W (Unicode) and _DOC_INFO_1A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOC_INFO_1W, *PDOC_INFO_1W, *LPDOC_INFO_1W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DOC_INFO_1
-	_DOC_INFO_1A
-	_DOC_INFO_1W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOC_INFO_1W structure


## -description



The <b>DOC_INFO_1</b> structure describes a document that will be printed.




## -struct-fields




### -field pDocName

Pointer to a null-terminated string that specifies the name of the document.


### -field pOutputFile

Pointer to a null-terminated string that specifies the name of an output file. To print to a printer, set this to <b>NULL</b>.


### -field pDatatype

Pointer to a null-terminated string that identifies the type of data used to record the document.


## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>
 

 

