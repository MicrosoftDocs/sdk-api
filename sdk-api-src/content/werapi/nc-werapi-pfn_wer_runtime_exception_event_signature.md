---
UID: NC:werapi.PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE
title: PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE
author: windows-sdk-content
description: WER can call this function multiple times to get the report parameters that uniquely describe the problem.
old-location: wer\outofprocessexceptioneventsignaturecallback.htm
old-project: wer
ms.assetid: 892498db-0265-4276-9735-63a8104ecaa9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: OutOfProcessExceptionEventSignatureCallback, OutOfProcessExceptionEventSignatureCallback callback function [Windows Error Reporting], PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE, PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE callback, wer.outofprocessexceptioneventsignaturecallback, werapi/OutOfProcessExceptionEventSignatureCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: werapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Werapi.h
api_name:
 - OutOfProcessExceptionEventSignatureCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE callback function


## -description


 WER can call this function multiple times to get the report parameters that uniquely describe the problem.

The <b>PFN_WER_RUNTIME_EXCEPTION_EVENT_SIGNATURE</b> type defines a pointer to this callback function. You must use "OutOfProcessExceptionEventSignatureCallback" as the name of the callback function.


## -parameters




### -param pContext [in]

A pointer to arbitrary context information that you specified when you called the <a href="https://msdn.microsoft.com/b0fb2c0d-cc98-43cc-a508-e80545377b7f">WerRegisterRuntimeExceptionModule</a> function to register the exception handler.


### -param pExceptionInformation [in]

A <a href="https://msdn.microsoft.com/fcf956ac-6015-439c-aec6-8f6a826ff269">WER_RUNTIME_EXCEPTION_INFORMATION</a> structure that contains the exception information.


### -param dwIndex [in]

The index of the report parameter. Valid values are 0 to 9. The first call to this function must set the index to 0, and each successive call must increment the index value sequentially.


### -param pwszName [out]

A caller-allocated buffer that you use to specify the parameter name.


### -param pchName [in, out]

The size, in characters, of the <i>pwszName</i> buffer. The size includes the null-terminating character.


### -param pwszValue [out]

A caller-allocated buffer that you use to specify the parameter value. 


### -param pchValue [in, out]

The size, in characters, of the <i>pwszValue</i> buffer. The size includes the null-terminating character.


## -returns



Return <b>S_OK</b> on success. If you return other failure codes, WER reverts to its default crash reporting behavior.




## -remarks



You must implement this function in your exception handler DLL.

To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called report parameters. Report parameters include information such as the application name, application version, module name, module version, and error code. The combination of these report parameters describes a unique problem.

WER calls this callback function only if you set the <i>pbOwnershipClaimed</i> parameter of your <a href="https://msdn.microsoft.com/22033278-2be3-4621-b618-3ccd21fb4cdd">OutOfProcessExceptionEventCallback</a> callback function to <b>TRUE</b>. The <i>pdwSignatureCount</i> parameter of <b>OutOfProcessExceptionEventCallback</b> determines the number of times that  WER will call  this callback function.




## -see-also




<a href="https://msdn.microsoft.com/b0fb2c0d-cc98-43cc-a508-e80545377b7f">WerRegisterRuntimeExceptionModule</a>
 

 

