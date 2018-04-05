---
UID: NF:winspool.GetSpoolFileHandle
title: GetSpoolFileHandle function
author: windows-driver-content
description: The GetSpoolFileHandle function retrieves a handle for the spool file associated with the job currently submitted by the application.
old-location: gdi\getspoolfilehandle.htm
old-project: printdocs
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetSpoolFileHandle, GetSpoolFileHandle function [Windows GDI], GetSpoolFileHandleA, GetSpoolFileHandleW, _win32_GetSpoolFileHandle, gdi.getspoolfilehandle, winspool/GetSpoolFileHandle, winspool/GetSpoolFileHandleA, winspool/GetSpoolFileHandleW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSpoolFileHandleW (Unicode) and GetSpoolFileHandleA (ANSI)
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
-	WinSpool.drv
api_name:
-	GetSpoolFileHandle
-	GetSpoolFileHandleA
-	GetSpoolFileHandleW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetSpoolFileHandle function


## -description


The <b>GetSpoolFileHandle</b> function retrieves a handle for the spool file associated with the job currently submitted by the application.


## -parameters




### -param hPrinter [in]

A handle to the printer to which the job was submitted. This should be the same handle that was used to submit the job. (Use the <a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a> or <a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a> function to retrieve a printer handle.)


## -returns



If the function succeeds, it returns a handle to the spool file.

If the function fails, it returns <b>INVALID_HANDLE_VALUE</b>.




## -remarks



With the handle to the spool file, your application can write to the spool file with calls to <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> followed by <a href="https://msdn.microsoft.com/cb8899e0-2fdf-4928-adff-17ef5af39f63">CommitSpoolData</a>.

Your application must not call <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a> on <i>hPrinter</i> until after it has accessed the spool file for the last time. Then it should call <a href="https://msdn.microsoft.com/e2c0e68f-b72e-4a97-ba18-8943bc5789c1">CloseSpoolFileHandle</a> followed by <b>ClosePrinter</b>. Attempts to access the spool file handle after the original <i>hPrinter</i> has been closed will fail even if the file handle itself has not been closed. <b>CloseSpoolFileHandle</b> will itself fail if <b>ClosePrinter</b> is called first.

This function will fail if it is called before the print job has finished spooling.




## -see-also




<a href="https://msdn.microsoft.com/ffc4fee8-46c6-47ad-803d-623bf8efdefd">AddPrinter</a>



<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/e2c0e68f-b72e-4a97-ba18-8943bc5789c1">CloseSpoolFileHandle</a>



<a href="https://msdn.microsoft.com/cb8899e0-2fdf-4928-adff-17ef5af39f63">CommitSpoolData</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

