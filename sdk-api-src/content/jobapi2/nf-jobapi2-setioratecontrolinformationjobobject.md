---
UID: NF:jobapi2.SetIoRateControlInformationJobObject
title: SetIoRateControlInformationJobObject function
author: windows-driver-content
description: Sets I/O limits on a job object.
old-location: base\setioratecontrolinformationjobobject.htm
old-project: ProcThread
ms.assetid: 7E108E01-6D43-4336-BFE0-5EE655FD5D45
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SetIoRateControlInformationJobObject, SetIoRateControlInformationJobObject function, base.setioratecontrolinformationjobobject, jobapi2/SetIoRateControlInformationJobObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: jobapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.typenames: AM_WST_PAGE, *PAM_WST_PAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-Job-L2-1-1.dll
-	Kernel32Legacy.dll
api_name:
-	SetIoRateControlInformationJobObject
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIoRateControlInformationJobObject function


## -description


Sets I/O limits on a job object.


## -parameters




### -param hJob [in]

A handle to the job on which to set I/O limits. Get this handle from the <a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> or <a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a> function. The handle must have the <b>JOB_OBJECT_SET_ATTRIBUTES</b> access right. For more information about access rights, see <a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>.


### -param IoRateControlInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/E4AA03B5-4D83-4826-B85D-FA4B412AFEBF">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a> structure that specifies the I/O limits to set for the job.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<div class="alert"><b>Important</b>  Starting with Windows 10, version 1607, this function is no longer supported.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/E4AA03B5-4D83-4826-B85D-FA4B412AFEBF">JOBOBJECT_IO_RATE_CONTROL_INFORMATION</a>



<a href="https://msdn.microsoft.com/B61DA8FC-1CF7-4D97-86F5-E3C2131D41EC">QueryIoRateControlInformationJobObject</a>
 

 

