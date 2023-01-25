---
UID: NF:securitybaseapi.SetCachedSigningLevel
tech.root: security
title: SetCachedSigningLevel (securitybaseapi.h)
ms.date: 12/02/2022
targetos: Windows
description: Sets the cached signing level.
ms.keywords: SetCachedSigningLevel
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
topic_type:
 - apiref
api_type:
 - 
api_location:
 - securitybaseapi.h
api_name:
 - SetCachedSigningLevel
f1_keywords:
 - SetCachedSigningLevel
 - securitybaseapi/SetCachedSigningLevel
dev_langs:
 - c++
helpviewer_keywords:
 - SetCachedSigningLevel
---

# SetCachedSigningLevel function (securitybaseapi.h)

## -description

Sets the cached signing level.

## -parameters

### -param SourceFiles [in]

Pointer to a set of source file handles.

### -param SourceFileCount [in]

The source file count.

### -param Flags [in]

Pointer to the flags set on the file.

### -param TargetFile [in, optional]

The target file.

## -returns

If the function succeeds, it returns **TRUE**.

If the function fails, it returns **FALSE**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** may return one of the error codes defined in WinError.h.

## -remarks

## -see-also

[GetCachedSigningLevel](nf-securitybaseapi-getcachedsigninglevel.md)
