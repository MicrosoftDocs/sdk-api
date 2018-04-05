---
UID: NS:winspool._DOC_INFO_3A
title: "_DOC_INFO_3A"
author: windows-driver-content
description: The DOC_INFO_3 structure describes a document that will be printed.
old-location: gdi\doc_info_3.htm
old-project: printdocs
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPDOC_INFO_3A, *PDOC_INFO_3A, DOC_INFO_3, DOC_INFO_3 structure [Windows GDI], DOC_INFO_3A, PDOC_INFO_3, PDOC_INFO_3 structure pointer [Windows GDI], _DOC_INFO_3A, _DOC_INFO_3W, _win32_DOC_INFO_3_str, gdi.doc_info_3, winspool/DOC_INFO_3, winspool/PDOC_INFO_3, winspool/_DOC_INFO_3A, winspool/_DOC_INFO_3W"
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
req.unicode-ansi: "_DOC_INFO_3W (Unicode) and _DOC_INFO_3A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOC_INFO_3A, *PDOC_INFO_3A, *LPDOC_INFO_3A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	DOC_INFO_3
-	_DOC_INFO_3A
-	_DOC_INFO_3W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOC_INFO_3A structure


## -description



The <b>DOC_INFO_3</b> structure describes a document that will be printed.




## -struct-fields




### -field pDocName

Pointer to a null-terminated string that specifies the name of the document.


### -field pOutputFile

Pointer to a null-terminated string that specifies the name of an output file.


### -field pDatatype

Pointer to a null-terminated string that identifies the type of data used to record the document.


### -field dwFlags

Flags. Currently, it can be <b>NULL</b> or the following.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>DI_MEMORYMAP_WRITE</td>
<td>Causes <a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a> to not use <a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a> and <a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a> for local printing.</td>
</tr>
</table>
 


## -remarks



The DI_MEMORYMAP_WRITE setting in <b>DOC_INFO_3</b> is an optimization. This allows GDI to map spool files in the application and speed up the recording.




## -see-also




<a href="https://msdn.microsoft.com/cfafa874-6022-4bf4-bf3d-096213eb0c98">AddJob</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/a103a29c-be4d-491e-9b04-84571fe969a5">ScheduleJob</a>



<a href="https://msdn.microsoft.com/caa2bd80-4af3-4968-a5b9-d12f16cac6fc">StartDocPrinter</a>
 

 

