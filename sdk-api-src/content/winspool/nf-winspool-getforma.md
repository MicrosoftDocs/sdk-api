---
UID: NF:winspool.GetFormA
title: GetFormA function
author: windows-driver-content
description: The GetForm function retrieves information about a specified form.
old-location: gdi\getform.htm
old-project: printdocs
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetForm, GetForm function [Windows GDI], GetFormA, GetFormW, _win32_GetForm, gdi.getform, winspool/GetForm, winspool/GetFormA, winspool/GetFormW
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
req.unicode-ansi: GetFormW (Unicode) and GetFormA (ANSI)
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
-	GetForm
-	GetFormA
-	GetFormW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetFormA function


## -description


The <b>GetForm</b> function retrieves information about a specified form.


## -parameters




### -param hPrinter [in]

A handle to the printer. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pFormName [in]

A pointer to a null-terminated string that specifies the name of the form. To get the names of the forms supported by the printer, call the <a href="https://msdn.microsoft.com/b13b515a-c764-4a80-ab85-95fb4abb2a6b">EnumForms</a> function.


### -param Level [in]

The version of the structure to which <i>pForm</i> points. This value must be 1 or 2.


### -param pForm [out]

A pointer to an array of bytes that receives the initialized <a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a> or <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> structure.


### -param cbBuf [in]

The size, in bytes, of the <i>pForm</i> array.


### -param pcbNeeded [out]

A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if <i>cbBuf</i> is too small.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
If the caller is remote, and the <i>Level</i> is 2, the <b>StringType</b> value of the returned <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> will always be STRING_LANGPAIR.




## -see-also




<a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a>



<a href="https://msdn.microsoft.com/a2d0345f-2469-46ab-935f-777f2b33b621">DeleteForm</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/05d5d495-952c-4a1d-8694-1004d0c2bcf6">SetForm</a>
 

 

