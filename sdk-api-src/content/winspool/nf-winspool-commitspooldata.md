---
UID: NF:winspool.CommitSpoolData
title: CommitSpoolData function
author: windows-driver-content
description: The CommitSpoolData function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.
old-location: gdi\commitspooldata.htm
old-project: printdocs
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CommitSpoolData, CommitSpoolData function [Windows GDI], _win32_CommitSpoolData, gdi.commitspooldata, winspool/CommitSpoolData
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
-	CommitSpoolData
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: WinSpool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CommitSpoolData function


## -description


The <b>CommitSpoolData</b> function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.


## -parameters




### -param hPrinter [in]

A handle to the printer to which the job was submitted. This should be the same handle that was used to obtain <i>hSpoolFile</i> with <a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a>.


### -param hSpoolFile [in]

A handle to the spool file being changed. On the first call of <b>CommitSpoolData</b>, this should be the same handle that was returned by <a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a>. Subsequent calls to <b>CommitSpoolData</b> should pass the handle returned by the preceding call. See Remarks.


### -param cbCommit

The number of bytes committed to the print spooler.


## -returns



If the function succeeds, it returns a handle to the spool file.

If the function fails, it returns INVALID_HANDLE_VALUE.




## -remarks



Applications submitting a spooler print job can call <a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a> and then directly write data to the spool file handle by calling <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>. To notify the print spooler that the file contains data which is ready to be rendered, the application must call <b>CommitSpoolData</b> and provide the number of available bytes.

If <b>CommitSpoolData</b> is called multiple times, each call must use the spool file handle returned by the previous call. When no more data will be written to the spool file, <a href="https://msdn.microsoft.com/e2c0e68f-b72e-4a97-ba18-8943bc5789c1">CloseSpoolFileHandle</a> should be called for the file handle returned by the last call to <b>CommitSpoolData</b>.

Before calling <b>CommitSpoolData</b>, applications must set the file pointer to the position it had before it wrote data to the file. In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer <i>cbCommit</i> bytes from the current value of file pointer.




## -see-also




<a href="https://msdn.microsoft.com/e2c0e68f-b72e-4a97-ba18-8943bc5789c1">CloseSpoolFileHandle</a>



<a href="https://msdn.microsoft.com/df6f28b3-66a6-4fb7-bdde-40cd7d934c5f">GetSpoolFileHandle</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

