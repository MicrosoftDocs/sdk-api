---
UID: NF:winspool.DeleteFormA
title: DeleteFormA function
author: windows-driver-content
description: The DeleteForm function removes a form name from the list of supported forms.
old-location: gdi\deleteform.htm
old-project: printdocs
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: DeleteForm, DeleteForm function [Windows GDI], DeleteFormA, DeleteFormW, _win32_DeleteForm, gdi.deleteform, winspool/DeleteForm, winspool/DeleteFormA, winspool/DeleteFormW
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
req.unicode-ansi: DeleteFormW (Unicode) and DeleteFormA (ANSI)
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
-	DeleteForm
-	DeleteFormA
-	DeleteFormW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DeleteFormA function


## -description


The <b>DeleteForm</b> function removes a form name from the list of supported forms.


## -parameters




### -param hPrinter [in]

Indicates the open printer handle that this function is to be performed upon. Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.


### -param pFormName [in]

Pointer to the form name to be removed.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. 




## -remarks



<div class="alert"><b>Note</b>  This is a blocking or synchronous function and might not return immediately. How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation—factors that are difficult to predict when writing an application. Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</div>
<div> </div>
<b>DeleteForm</b> can only delete form names that were added by using the <a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a> function.




## -see-also




<a href="https://msdn.microsoft.com/17b59019-f93a-4b57-86fb-91c61aecbac4">AddForm</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

