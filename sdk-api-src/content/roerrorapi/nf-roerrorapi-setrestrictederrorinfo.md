---
UID: NF:roerrorapi.SetRestrictedErrorInfo
title: SetRestrictedErrorInfo function
description: Sets the restricted error information object for the current thread.
helpviewer_keywords: ["SetRestrictedErrorInfo","SetRestrictedErrorInfo function [Windows Runtime]","roerrorapi/SetRestrictedErrorInfo","winrt.setrestrictederrorinfo"]
old-location: winrt\setrestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: 3F4A62EF-ECD3-45FA-836D-77C510C43C5E
ms.date: 12/5/2018
ms.keywords: SetRestrictedErrorInfo, SetRestrictedErrorInfo function [Windows Runtime], roerrorapi/SetRestrictedErrorInfo, winrt.setrestrictederrorinfo
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - SetRestrictedErrorInfo
 - roerrorapi/SetRestrictedErrorInfo
dev_langs:
 - c++
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
---

# SetRestrictedErrorInfo function


## -description

Sets the restricted error information object for the current thread.

## -parameters

### -param pRestrictedErrorInfo [in]

The restricted error information object associated with the current thread.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> function to save error information for the current thread in a Windows Store app. Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a> function to raise an exception, terminate the current process, and report the error to the Windows Error Reporting service (WER).

The <b>SetRestrictedErrorInfo</b>  function calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to find the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a> object, and then it calls <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>.   The call fails if <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> isn't the system implementation. To create an <b>IRestrictedErrorInfo</b> object, call  the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">OriginateError</a>, <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">TransformError</a>, or <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> functions.

The <b>SetRestrictedErrorInfo</b>  function releases the existing restricted error information object, if one exists, and sets <i>pRestrictedErrorInfo</i>.  For more info, see the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a> function.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>



<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-seterrorinfo">SetErrorInfo</a>