---
UID: NF:securitybaseapi.GetCachedSigningLevel
tech.root: security
title: GetCachedSigningLevel (securitybaseapi.h)
ms.date: 12/02/2022
ms.keywords: GetCachedSigningLevel
targetos: Windows
description: Retrieves the cached signing level.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Advapi32.dll
req.header: securitybaseapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Advapi32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
targetos: Windows
topic_type:
 - apiref
api_type:
 - 
api_location:
 - securitybaseapi.h
api_name:
 - GetCachedSigningLevel
f1_keywords:
 - GetCachedSigningLevel
 - securitybaseapi/GetCachedSigningLevel
dev_langs:
 - c++
helpviewer_keywords:
 - GetCachedSigningLevel
---

# GetCachedSigningLevel function (securitybaseapi.h)

## -description

Retrieves the cached signing level.

## -parameters

### -param File [in]

Handle to a file.

### -param Flags [Out]

Pointer to the flags set on the file.

### -param SigningLevel [Out]

Pointer ot the signing level.

### -param Thumbprint [Out, optional]

Pointer to the thumbprint.

### -param ThumbprintSize [In, Out, optional]

Pointer to the thumbprint size.

### -param ThumbprintAlgorithm [Out, optional]

Pointer to the thumbprint algorithm.

## -returns

If the function succeeds, it returns **TRUE**.

If the function fails, it returns **FALSE**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** may return one of the following error codes defined in WinError.h.

## -remarks

## -see-also

[SetCachedSigningLevel](nf-securitybaseapi-setcachedsigninglevel.md)