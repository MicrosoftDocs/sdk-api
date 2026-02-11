---
UID: NF:wtsapi32.WTSCloudAuthGetServerNonce
tech.root: TermServ
title: WTSCloudAuthGetServerNonce
ms.date: 09/25/2025
targetos: Windows
description: Requests a server nonce from the Cloud Authentication security support provider.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wtsapi32.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wtsapi32.dll
api_name:
 - WTSCloudAuthGetServerNonce
f1_keywords:
 - WTSCloudAuthGetServerNonce
 - wtsapi32/WTSCloudAuthGetServerNonce
dev_langs:
 - c++
helpviewer_keywords:
 - WTSCloudAuthGetServerNonce
---

## -description

Requests a server nonce from the Cloud Authentication security support provider.

## -parameters

### -param cloudAuthHandle [in]

The cloud authentication handle obtained by calling *WTSCloudAuthOpen*.

### -param serverNonce [out]

Receives the generated server nonce if the function succeeds. To free the allocated memory, call the *[WTSFreeMemoryEx](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsfreememoryexw)* function and pass *WTSTypeCloudAuthServerNonce* for the *WTSTypeClass* parameter.

## -returns

If the function succeeds, the return value is a nonzero value. If the function fails, the return value is zero. To get extended error information, call the [`GetLastError`](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

The server nonce is required to build an [assertion](/openspecs/windows_protocols/ms-rdpbcgr/ba819b6b-257a-466f-b8e5-f262d78677f7) to authenticate to the server when using Entra authentication. The caller is responsible for transporting the server nonce to the client to use for the purposes of constructing the assertion.

## -see-also
