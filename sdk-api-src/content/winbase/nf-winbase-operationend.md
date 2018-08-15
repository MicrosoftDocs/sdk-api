---
UID: NF:winbase.OperationEnd
title: OperationEnd function
author: windows-sdk-content
description: Notifies the system that the application is about to end an operation.
old-location: oprec\operationend.htm
old-project: oprec
ms.assetid: 73C6FBDD-BB4A-46A5-8E39-7862A1938F47
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OperationEnd, OperationEnd function [Operation Recorder], oprec.operationend, winbase/OperationEnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - OperationEnd
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OperationEnd function


## -description


Notifies the system that the application is about to end an operation

Every call to <a href="https://msdn.microsoft.com/3E67057E-D09F-48BA-A95A-5D00F4783D9C">OperationStart</a> must be followed by a call to <b>OperationEnd</b>, otherwise the operation's record of file access patterns is discarded after 10 seconds.


## -parameters




### -param OperationEndParams [in]

An <a href="https://msdn.microsoft.com/45ABFE6A-7B70-418F-8C3C-6388079D1306">_OPERATION_END_PARAMETERS</a> structure that specifies <b>VERSION</b>, <b>OPERATION_ID</b> and <b>FLAGS</b>.


## -returns



<b>TRUE</b> for all valid parameters and <b>FALSE</b> otherwise.  To get extended error information, call <b>GetLastError</b>. 




## -remarks



The version of the <a href="https://msdn.microsoft.com/45ABFE6A-7B70-418F-8C3C-6388079D1306">_OPERATION_END_PARAMETERS</a> structure is defined as <b>OPERATION_API_VERSION</b> in the Windows SDK. 

The  <b>OperationEnd</b> function is safe to call on any thread.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/D5446D23-DBB5-4EB8-97E4-590537A33193">OPERATION_ID</a>



<a href="https://msdn.microsoft.com/c1051b62-0e67-4480-81c6-cb138d3296d6">Operation Recorder</a>



<a href="https://msdn.microsoft.com/3E67057E-D09F-48BA-A95A-5D00F4783D9C">OperationStart</a>



<a href="https://msdn.microsoft.com/45ABFE6A-7B70-418F-8C3C-6388079D1306">_OPERATION_END_PARAMETERS</a>



<a href="https://msdn.microsoft.com/51AE0017-2CDE-4BCD-AE03-B366343DE558">_OPERATION_START_PARAMETERS</a>
 

 

