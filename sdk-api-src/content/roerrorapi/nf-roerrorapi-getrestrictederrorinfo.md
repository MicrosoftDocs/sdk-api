---
UID: NF:roerrorapi.GetRestrictedErrorInfo
title: GetRestrictedErrorInfo function
description: Gets the restricted error information object set by a previous call to SetRestrictedErrorInfo in the current logical thread.
helpviewer_keywords: ["GetRestrictedErrorInfo","GetRestrictedErrorInfo function [Windows Runtime]","roerrorapi/GetRestrictedErrorInfo","winrt.getrestrictederrorinfo"]
old-location: winrt\getrestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: CA459E57-90D5-44F6-A896-4E1C2FA0DC57
ms.date: 12/5/2018
ms.keywords: GetRestrictedErrorInfo, GetRestrictedErrorInfo function [Windows Runtime], roerrorapi/GetRestrictedErrorInfo, winrt.getrestrictederrorinfo
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
req.lib: 
req.dll: Combase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - GetRestrictedErrorInfo
 - roerrorapi/GetRestrictedErrorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - API-MS-Win-Core-Winrt-error-l1-1-0.dll
 - API-MS-Win-Core-Winrt-error-l1-1-1.dll
api_name:
 - GetRestrictedErrorInfo
---

# GetRestrictedErrorInfo function


## -description

Gets the restricted error information object set by a previous call to <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo">SetRestrictedErrorInfo</a> in the current logical thread.

## -parameters

### -param ppRestrictedErrorInfo [out]

The restricted error info object associated with the current thread.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  restricted error object was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no restricted error object associated with the current thread. Any other error object is removed from the thread.

</td>
</tr>
</table>

## -remarks

Call the <b>GetRestrictedErrorInfo</b>  function to get the most recently set <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> object on the current thread in a Windows Store app.

Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> function to save error information for the current thread. Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a> function to raise an exception, terminate the current process, and report the error to the Windows Error Reporting service (WER).

<b>GetRestrictedErrorInfo</b> transfers ownership of the error object to the caller and clears the error state for the thread. If the most recently set error object doesn't support the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> interface, the error state for the thread is cleared, but no interface is returned to the caller.

The <b>GetRestrictedErrorInfo</b> retrieves the error object from the current thread and calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to find the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> interface.  If <b>IRestrictedErrorInfo</b> isn't found, <b>GetRestrictedErrorInfo</b> returns <b>S_FALSE</b>.  In this case, the error object is removed from the thread. For more info, see <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

Calling the <b>GetRestrictedErrorInfo</b>  function fails if <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> isn't the system implementation. To create an <b>IRestrictedErrorInfo</b> object, call  the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginateerror">OriginateError</a>, <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rotransformerror">TransformError</a>, or <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> functions.

## -see-also

<a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>



<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>



<a href="/windows/desktop/api/roerrorapi/ne-roerrorapi-roerrorreportingflags">RO_ERROR_REPORTING_FLAGS</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext">RoFailFastWithErrorContext</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo">SetRestrictedErrorInfo</a>