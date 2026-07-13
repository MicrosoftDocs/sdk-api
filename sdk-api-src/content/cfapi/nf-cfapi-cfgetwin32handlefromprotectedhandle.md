---
UID: NF:cfapi.CfGetWin32HandleFromProtectedHandle
title: CfGetWin32HandleFromProtectedHandle function (cfapi.h)
description: Converts a protected handle to a Win32 handle so that it can be used with all handle-based Win32 APIs.
helpviewer_keywords: ["CfGetWin32HandleFromProtectedHandle","CfGetWin32HandleFromProtectedHandle function","cfapi/CfGetWin32HandleFromProtectedHandle","cloudApi.cfgetwin32handlefromprotectedhandle"]
old-location: cloudapi\cfgetwin32handlefromprotectedhandle.htm
tech.root: cloudapi
ms.assetid: 8C54B6F3-7709-4021-8965-E96B74DD3319
ms.date: 03/30/2023
ms.keywords: CfGetWin32HandleFromProtectedHandle, CfGetWin32HandleFromProtectedHandle function, cfapi/CfGetWin32HandleFromProtectedHandle, cloudApi.cfgetwin32handlefromprotectedhandle
req.header: cfapi.h
req.include-header: 
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfGetWin32HandleFromProtectedHandle
 - cfapi/CfGetWin32HandleFromProtectedHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfGetWin32HandleFromProtectedHandle
---

# CfGetWin32HandleFromProtectedHandle function

## -description

Converts a protected handle to a Win32 handle so that it can be used with all handle-based Win32 APIs.

## -parameters

### -param ProtectedHandle [in]

The protected handle to be converted.

## -returns

The corresponding Win32 handle.

## -remarks

The caller must have referenced the protected handle prior to this call using [CfReferenceProtectedHandle](nf-cfapi-cfreferenceprotectedhandle.md) to ensure that the use of the Win32 handle is tracked, and the Win32 API call that consumes the Win32 handle is synchronized with the oplock break notification acknowledgment.

The caller must release the reference on the protected handle after being done with the Win32 handle using [CfReleaseProtectedHandle](nf-cfapi-cfreleaseprotectedhandle.md).

In no circumstances should the caller close the Win32 handle returned using [CfCloseHandle](nf-cfapi-cfclosehandle.md).

## -see-also

[CfReferenceProtectedHandle](nf-cfapi-cfreferenceprotectedhandle.md)

[CfReleaseProtectedHandle](nf-cfapi-cfreleaseprotectedhandle.md)

[CfCloseHandle](nf-cfapi-cfclosehandle.md)
