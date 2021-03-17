---
UID: NF:winnls.LoadStringByReference
title: LoadStringByReference function (winnls.h)
description: Unsupported. LoadStringByReference may be altered or unavailable. Instead, use SHLoadIndirectString.
helpviewer_keywords: ["LoadStringByReference","LoadStringByReference function [Internationalization for Windows Applications]","intl.loadstringbyreference","winnls/LoadStringByReference"]
old-location: intl\loadstringbyreference.htm
tech.root: Intl
ms.assetid: 4E0470ED-512F-4B76-A3E4-31C8B269CD5C
ms.date: 12/05/2018
ms.keywords: LoadStringByReference, LoadStringByReference function [Internationalization for Windows Applications], intl.loadstringbyreference, winnls/LoadStringByReference
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadStringByReference
 - winnls/LoadStringByReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Localization-private-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - LoadStringByReference
---

# LoadStringByReference function


## -description

Unsupported. <b>LoadStringByReference</b> may be altered or unavailable. Instead, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shloadindirectstring">SHLoadIndirectString</a>.

## -parameters

### -param Flags [in]

Reserved.

### -param Language [in, optional]

The language.

### -param SourceString [in]

The source string reference.

### -param Buffer [out, optional]

The buffer to receive the string.

### -param cchBuffer [in]

The size of <i>Buffer</i>, in characters.

### -param Directory [in, optional]

The directory path to <i>SourceString</i>.

### -param pcchBufferOut [out, optional]

The number of characters written to <i>Buffer</i>.

## -returns

A <b>BOOL</b> datatype.

## -remarks

<b>LoadStringByReference</b> is not supported and may be altered or unavailable in the future. Instead, use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shloadindirectstring">SHLoadIndirectString</a>.