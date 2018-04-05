---
UID: NF:winspool.EnumFormsA
title: EnumFormsA function
author: windows-driver-content
description: The EnumForms function enumerates the forms supported by the specified printer.
old-location: gdi\enumforms.htm
old-project: printdocs
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EnumForms, EnumForms function [Windows GDI], EnumFormsA, EnumFormsW, _win32_EnumForms, gdi.enumforms, winspool/EnumForms, winspool/EnumFormsA, winspool/EnumFormsW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFormsW (Unicode) and EnumFormsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
api_name:
-	EnumForms
-	EnumFormsA
-	EnumFormsW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EnumFormsA function


## -description


The <b>EnumForms</b> function enumerates the forms supported by the specified printer.


## -parameters




### -param hPrinter [in]

Handle to the printer for which the forms should be enumerated. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param Level [in]

Specifies the version of the structure to which <i>pForm</i> points. This value must be 1 or 2.


### -param pForm [out]

Pointer to one or more <a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a> structures or to one or more <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> structures. All the structures will have the same level.


### -param cbBuf [in]

Specifies the size, in bytes, of the buffer to which <i>pForm</i> points.


### -param pcbNeeded [out]

Pointer to a variable that receives the number of bytes copied to the array to which <i>pForm</i> points (if the operation succeeds) or the number of bytes required (if it fails because <i>cbBuf</i> is too small).


### -param pcReturned [out]

Pointer to a variable that receives the number of structures copied into the array to which <i>pForm</i> points.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If the caller is remote, and the <i>Level</i> is 2, the <b>StringType</b> value of the returned <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> structures will always be <b>STRING_LANGPAIR</b>.

In Windows Vista, the form data returned by <b>EnumForms</b> is retrieved from a local cache when <i>hPrinter</i> refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server. In all other configurations, the form data is queried from the remote print server.




## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

