---
UID: NF:shlwapi.StrCpyW
title: StrCpyW function (shlwapi.h)
description: Copies one string to another. (StrCpyW)
helpviewer_keywords: ["StrCpy","StrCpy function [Windows Shell]","StrCpyW","_win32_StrCpy","shell.StrCpy","shlwapi/StrCpy","shlwapi/StrCpyW"]
old-location: shell\StrCpy.htm
tech.root: shell
ms.assetid: 83d1a8dc-fc43-4b06-b36c-c9c91d779d25
ms.date: 12/05/2018
ms.keywords: StrCpy, StrCpy function [Windows Shell], StrCpyW, _win32_StrCpy, shell.StrCpy, shlwapi/StrCpy, shlwapi/StrCpyW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCpyW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrCpyW
 - shlwapi/StrCpyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StrCpy
 - StrCpyW
---

# StrCpyW function


## -description

Copies one string to another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters

### -param psz1 [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied string. This string is not guaranteed to be null-terminated.

### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated source string.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Consider using one of the following alternatives: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopya">StringCbCopy</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyexa">StringCbCopyEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopyna">StringCbCopyN</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcopynexa">StringCbCopyNEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopya">StringCchCopy</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyexa">StringCchCopyEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopyna">StringCchCopyN</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcopynexa">StringCchCopyNEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.
