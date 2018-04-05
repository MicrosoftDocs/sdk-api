---
UID: NF:winspool.CloseSpoolFileHandle
title: CloseSpoolFileHandle function
author: windows-driver-content
description: The CloseSpoolFileHandle function closes a handle to a spool file associated with the print job currently submitted by the application.
old-location: gdi\closespoolfilehandle.htm
old-project: printdocs
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CloseSpoolFileHandle, CloseSpoolFileHandle function [Windows GDI], _win32_CloseSpoolFileHandle, gdi.closespoolfilehandle, winspool/CloseSpoolFileHandle
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
req.unicode-ansi: 
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
-	CloseSpoolFileHandle
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CloseSpoolFileHandle function


## -description


The <b>CloseSpoolFileHandle</b> function closes a handle to a spool file associated with the print job currently submitted by the application.


## -parameters




### -param hPrinter [in]

A handle to the printer to which the job was submitted. This should be the same handle that was used to obtain <i>hSpoolFile</i> with <a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a>.


### -param hSpoolFile [in]

A handle to the spool file being closed. If <a href="https://msdn.microsoft.com/cb8899e0-2fdf-4928-adff-17ef5af39f63">CommitSpoolData</a> has not been called since <a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a> was called, then this should be the same handle that was returned by <b>GetSpoolFileHandle</b>. Otherwise, it should be the handle that was returned by the most recent call to <b>CommitSpoolData</b>.


## -returns



<b>TRUE</b>, if it succeeds, <b>FALSE</b> otherwise.




## -remarks



Your application must not call <a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a> on <i>hPrinter</i> until after it has accessed the spool file for the last time. Then it should call <b>CloseSpoolFileHandle</b> followed by <b>ClosePrinter</b>. Attempts to access the spool file handle after the original <i>hPrinter</i> has been closed will fail even if the file handle itself has not been closed. <b>CloseSpoolFileHandle</b> will fail if <b>ClosePrinter</b> is called first.




## -see-also




<a href="https://msdn.microsoft.com/95cc3eca-e65c-4fa6-8975-479e8e728dca">ClosePrinter</a>



<a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

