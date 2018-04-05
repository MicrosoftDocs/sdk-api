---
UID: NF:winspool.SetFormW
title: SetFormW function
author: windows-driver-content
description: The SetForm function sets the form information for the specified printer.
old-location: gdi\setform.htm
old-project: printdocs
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetForm, SetForm function [Windows GDI], SetFormA, SetFormW, _win32_SetForm, gdi.setform, winspool/SetForm, winspool/SetFormA, winspool/SetFormW
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
req.unicode-ansi: SetFormW (Unicode) and SetFormA (ANSI)
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
-	SetForm
-	SetFormA
-	SetFormW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetFormW function


## -description


The <b>SetForm</b> function sets the form information for the specified printer.


## -parameters




### -param hPrinter [in]

A handle to the printer for which the form information is set. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pFormName [in]

A pointer to a null-terminated string that specifies the form name for which the form information is set.


### -param Level [in]

The version of the structure to which <i>pForm</i> points. This value must be 1 or 2.


### -param pForm [in]

A pointer to a <a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a> or <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> structure.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>SetForm</b> can be called multiple times for an existing <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a>, each call adding additional pairs of <b>pDisplayName</b> and <b>wLangId</b> values. All languages versions of the form will get the <b>Size</b> and <b>ImageableArea</b> values of the <b>FORM_INFO_2</b> in the most recent call to <b>SetForm</b>.

If the caller is remote and the <i>Level</i> is 2, the <b>StringType</b> value of the <a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a> cannot be STRING_MUIDLL.




## -see-also




<a href="https://msdn.microsoft.com/1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7">FORM_INFO_1</a>



<a href="https://msdn.microsoft.com/5cc11a77-2b9d-44a4-88de-6ed0b7460bc8">FORM_INFO_2</a>



<a href="https://msdn.microsoft.com/10b25748-6d7c-46ab-bd2c-9b6126a1d7d1">GetForm</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

