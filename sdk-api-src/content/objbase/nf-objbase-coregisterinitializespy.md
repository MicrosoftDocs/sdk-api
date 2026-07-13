---
UID: NF:objbase.CoRegisterInitializeSpy
title: CoRegisterInitializeSpy function (objbase.h)
description: Registers an implementation of the IInitializeSpy interface. The IInitializeSpy interface is defined to allow developers to perform initialization and cleanup on COM apartments.
helpviewer_keywords: ["CoRegisterInitializeSpy","CoRegisterInitializeSpy function [COM]","_com_CoRegisterInitializeSpy","com.coregisterinitializespy","objbase/CoRegisterInitializeSpy"]
old-location: com\coregisterinitializespy.htm
tech.root: com
ms.assetid: 1fd5606e-0a15-429a-b656-4620b873bec5
ms.date: 12/05/2018
ms.keywords: CoRegisterInitializeSpy, CoRegisterInitializeSpy function [COM], _com_CoRegisterInitializeSpy, com.coregisterinitializespy, objbase/CoRegisterInitializeSpy
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterInitializeSpy
 - objbase/CoRegisterInitializeSpy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-private-l1-3-1.dll
 - api-ms-win-core-com-private-l1-3-0.dll
 - api-ms-win-core-com-private-l1-2-0.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoRegisterInitializeSpy
---

## -description

Registers an implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> interface. The <b>IInitializeSpy</b> interface is defined to allow developers to perform initialization and cleanup on COM apartments.

## -parameters

### -param pSpy [in]

A pointer to an instance of the <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> implementation.

### -param puliCookie [out]

The address at which to store a cookie that identifies this registration.

## -returns

This function can return the standard return value E_INVALIDARG, as well as the following values.

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
The object was successfully registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>.

</td>
</tr>
</table>

## -remarks

The <b>CoRegisterInitializeSpy</b> function registers an implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> interface, which defines methods to be called when <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> (or <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>) or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> is invoked.



<b>CoRegisterInitializeSpy</b> calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for IID_InitializeSpy on <i>pSpy</i>. It stores the address of the returned interface pointer in thread-specific storage that is independent of the COM initialization state for this thread. On success, it stores in <i>puliCookie</i> a <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a> cookie that represents this registration. Pass this cookie to <a href="/windows/desktop/api/objbase/nf-objbase-corevokeinitializespy">CoRevokeInitializeSpy</a> to revoke the registration.




<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> implementations must deal with nesting issues caused by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> from within a notification method. Notifications occur only after the registration happens on this thread. For example, if <b>CoInitializeEx</b> is called before <b>CoRegisterInitializeSpy</b>, then the <a href="/windows/desktop/api/objidl/nf-objidl-iinitializespy-preinitialize">PreInitialize</a> and <a href="/windows/desktop/api/objidl/nf-objidl-iinitializespy-postinitialize">PostInitialize</a> notification methods will not be called.



Notification methods must not cause the failure of <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> by throwing exceptions. Implementations of <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> must not propagate exceptions to code that calls <b>CoInitializeEx</b> or <b>CoUninitialize</b>. 



It is unpredictable whether a call to <b>CoRegisterInitializeSpy</b> from within an <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> method call will be effective during the current top-level (non-nested) call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>. A registered implementation of <b>IInitializeSpy</b> will always be effective for future top-level calls to <b>CoInitializeEx</b> or <b>CoUninitialize</b>.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-corevokeinitializespy">CoRevokeInitializeSpy</a>




<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>

