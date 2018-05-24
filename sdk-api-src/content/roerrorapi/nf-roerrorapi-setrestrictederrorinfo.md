---
UID: NF:roerrorapi.SetRestrictedErrorInfo
title: SetRestrictedErrorInfo function
author: windows-driver-content
description: Sets the restricted error information object for the current thread.
old-location: winrt\setrestrictederrorinfo.htm
old-project: WinRT
ms.assetid: 3F4A62EF-ECD3-45FA-836D-77C510C43C5E
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: SetRestrictedErrorInfo, SetRestrictedErrorInfo function [Windows Runtime], roerrorapi/SetRestrictedErrorInfo, winrt.setrestrictederrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComBase.dll
-	API-MS-Win-Core-WinRT-error-l1-1-0.dll
-	API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
-	SetRestrictedErrorInfo
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetRestrictedErrorInfo function


## -description


Sets the restricted error information object for the current thread.


## -parameters




### -param pRestrictedErrorInfo [in]

The restricted error information object associated with the current thread.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a> function to save error information for the current thread in a Windows Store app. Call the <a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a> function to raise an exception, terminate the current process, and report the error to the Windows Error Reporting service (WER).

The <b>SetRestrictedErrorInfo</b>  function calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to find the <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a> object, and then it calls <a href="https://msdn.microsoft.com/8eaacfac-fc37-4eaa-870b-10b99d598d66">SetErrorInfo</a>.   The call fails if <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> isn't the system implementation. To create an <b>IRestrictedErrorInfo</b> object, call  the <a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">OriginateError</a>, <a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">TransformError</a>, or <a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a> functions.

The <b>SetRestrictedErrorInfo</b>  function releases the existing restricted error information object, if one exists, and sets <i>pRestrictedErrorInfo</i>.  For more info, see the <a href="https://msdn.microsoft.com/8eaacfac-fc37-4eaa-870b-10b99d598d66">SetErrorInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a>



<a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a>



<a href="https://msdn.microsoft.com/8eaacfac-fc37-4eaa-870b-10b99d598d66">SetErrorInfo</a>
 

 

