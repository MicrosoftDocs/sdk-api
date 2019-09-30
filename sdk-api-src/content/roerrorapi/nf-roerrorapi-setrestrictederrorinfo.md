---
UID: NF:roerrorapi.SetRestrictedErrorInfo
title: SetRestrictedErrorInfo function
author: windows-sdk-content
description: Sets the restricted error information object for the current thread.
old-location: winrt\setrestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: 3F4A62EF-ECD3-45FA-836D-77C510C43C5E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetRestrictedErrorInfo, SetRestrictedErrorInfo function [Windows Runtime], roerrorapi/SetRestrictedErrorInfo, winrt.setrestrictederrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
f1_keywords: 
 - "roerrorapi/SetRestrictedErrorInfo"
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - SetRestrictedErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
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



Call the <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> function to save error information for the current thread in a Windows Store app. Call the <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a> function to raise an exception, terminate the current process, and report the error to the Windows Error Reporting service (WER).

The <b>SetRestrictedErrorInfo</b>  function calls <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> to find the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a> object, and then it calls <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>.   The call fails if <a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> isn't the system implementation. To create an <b>IRestrictedErrorInfo</b> object, call  the <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">OriginateError</a>, <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">TransformError</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> functions.

The <b>SetRestrictedErrorInfo</b>  function releases the existing restricted error information object, if one exists, and sets <i>pRestrictedErrorInfo</i>.  For more info, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/ne-roerrorapi-ro_error_reporting_flags">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>
 

 

