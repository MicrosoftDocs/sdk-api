---
UID: NF:objbase.CoRevokeInitializeSpy
title: CoRevokeInitializeSpy function (objbase.h)
description: Revokes a registered implementation of the IInitializeSpy interface.
helpviewer_keywords: ["CoRevokeInitializeSpy","CoRevokeInitializeSpy function [COM]","_com_CoRevokeInitializeSpy","com.corevokeinitializespy","objbase/CoRevokeInitializeSpy"]
old-location: com\corevokeinitializespy.htm
tech.root: com
ms.assetid: 24b0bedd-421a-4215-8edc-9fdce53e3b44
ms.date: 12/05/2018
ms.keywords: CoRevokeInitializeSpy, CoRevokeInitializeSpy function [COM], _com_CoRevokeInitializeSpy, com.corevokeinitializespy, objbase/CoRevokeInitializeSpy
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - CoRevokeInitializeSpy
 - objbase/CoRevokeInitializeSpy
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
 - CoRevokeInitializeSpy
---

# CoRevokeInitializeSpy function


## -description

Revokes a registered implementation of the <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> interface.

## -parameters

### -param uliCookie [in]

A <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer~r1">ULARGE_INTEGER</a> cookie identifying the registration.

## -returns

This function can return the standard return value E_INVALIDARG, as well as S_OK to indicate success.

## -remarks

<b>CoRevokeInitializeSpy</b> can only revoke cookies issued by previous calls to <a href="/windows/desktop/api/objbase/nf-objbase-coregisterinitializespy">CoRegisterInitializeSpy</a> that were executed on the current thread. Using a cookie from another thread, or one that corresponds to an already revoked registration, will return E_INVALIDARG.



It is unpredictable whether a call to <b>CoRevokeInitializeSpy</b> from within an <a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a> method call will have an effect during the current top-level (non-nested) call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>. The revocation will always have an effect after the current top-level call to <b>CoInitializeEx</b> or <b>CoUninitialize</b> returns.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coregisterinitializespy">CoRegisterInitializeSpy</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iinitializespy">IInitializeSpy</a>