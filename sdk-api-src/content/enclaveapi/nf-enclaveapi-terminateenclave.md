---
UID: NF:enclaveapi.TerminateEnclave
title: TerminateEnclave function
author: windows-sdk-content
description: Ends the execution of the threads that are running within an enclave.
old-location: base\terminateenclave.htm
old-project: memory
ms.assetid: D2BAF02F-AE05-43F2-BDB1-013EAF3AC653
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TerminateEnclave, TerminateEnclave function, base.terminateenclave, enclaveapi/TerminateEnclave
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: enclaveapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vertdll.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - TerminateEnclave
product: Windows
targetos: Windows
req.lib: Vertdll.lib
req.dll: Vertdll.dll; Api-ms-win-core-enclave-l1-1-0.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# TerminateEnclave function


## -description


Ends the execution of the threads that are running within  an enclave.


## -parameters




### -param lpAddress [in]

The base address of the enclave in which to end the execution of the threads.


### -param fWait [in]

<b>TRUE</b> if <b>TerminateEnclave</b> should not return  until all of the threads in the enclave end execution. <b>FALSE</b> if <b>TerminateEnclave</b> should return immediately.


## -returns



<b>TRUE</b> if the function succeeds; otherwise <b>FALSE</b>.  To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/4C495245-381F-4561-970D-5FCEC105276B">CallEnclave</a>
 

 

