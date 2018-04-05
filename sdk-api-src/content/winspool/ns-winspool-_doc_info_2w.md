---
UID: NS:winspool._DOC_INFO_2W
title: "_DOC_INFO_2W"
author: windows-driver-content
description: The DOC_INFO_2 structure describes a document that will be printed.
old-location: gdi\doc_info_2.htm
old-project: printdocs
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDOC_INFO_2W, *PDOC_INFO_2W, DOC_INFO_2, DOC_INFO_2 structure [Windows GDI], DOC_INFO_2W, PDOC_INFO_2, PDOC_INFO_2 structure pointer [Windows GDI], _DOC_INFO_2A, _DOC_INFO_2W, _win32_DOC_INFO_2_str, gdi.doc_info_2, winspool/DOC_INFO_2, winspool/PDOC_INFO_2, winspool/_DOC_INFO_2A, winspool/_DOC_INFO_2W"
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
req.unicode-ansi: "_DOC_INFO_2W (Unicode) and _DOC_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOC_INFO_2W, *PDOC_INFO_2W, *LPDOC_INFO_2W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DOC_INFO_2
-	_DOC_INFO_2A
-	_DOC_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOC_INFO_2W structure


## -description



The <b>DOC_INFO_2</b> structure describes a document that will be printed.




## -struct-fields




### -field pDocName

Pointer to a null-terminated string that specifies the name of the document.


### -field pOutputFile

Pointer to a null-terminated string that specifies the name of an output file.


### -field pDatatype

Pointer to a null-terminated string that identifies the type of data used to record the document.


### -field dwMode

Informs the print spooler of the nature of the data to follow. If this value is zero, the print spooler treats the data sent by subsequent calls to <a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a> as a normal print job (whether or not it is spooled depends on the printer property). If this value is DI_CHANNEL, only a communications channel is opened. In this case, the data passed into subsequent calls to <b>WritePrinter</b> is sent to the printer or subsequent calls to <a href="https://msdn.microsoft.com/d7c3f186-c53e-424b-89bf-6742babb998f">ReadPrinter</a> retrieve data from the printer. This mode remains effective until <a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a> is called.


### -field JobId

Reserved for internal use; should be zero.


## -see-also




<a href="https://msdn.microsoft.com/bf63ea0f-cc73-4943-9c84-52b3b77e141c">EndDoc</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/d7c3f186-c53e-424b-89bf-6742babb998f">ReadPrinter</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>



<a href="https://msdn.microsoft.com/9411b71f-d686-44ed-9051-d410e5ab228e">WritePrinter</a>
 

 

