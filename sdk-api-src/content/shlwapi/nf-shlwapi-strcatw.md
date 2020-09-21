---
UID: NF:shlwapi.StrCatW
title: StrCatW function (shlwapi.h)
description: Appends one string to another.
helpviewer_keywords: ["StrCat","StrCat function [Windows Shell]","StrCatW","_win32_StrCat","shell.StrCat","shlwapi/StrCat","shlwapi/StrCatW"]
old-location: shell\StrCat.htm
tech.root: shell
ms.assetid: fd357462-83be-42a8-9f39-1e023bd5f86e
ms.date: 12/05/2018
ms.keywords: StrCat, StrCat function [Windows Shell], StrCatW, _win32_StrCat, shell.StrCat, shlwapi/StrCat, shlwapi/StrCatW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrCatW (Unicode)
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
 - StrCatW
 - shlwapi/StrCatW
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
 - StrCat
 - StrCatW
---

# StrCatW function


## -description

Appends one string to another.
            
<div class="alert"><b>Note</b>  Do not use. See Remarks for alternative functions.</div><div> </div>

## -parameters

### -param psz1 [in, out]

Type: <b>PTSTR</b>

A pointer to a null-terminated string. When this function returns successfully, this string contains its original content with the string <i>psz2</i> appended. This buffer must be large enough to hold both strings and the terminating null character.

### -param psz2 [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string to be appended to <i>psz1</i>.

## -returns

Type: <b>PTSTR</b>

Returns a pointer to <i>psz1</i>, which holds the combined strings.

## -remarks

<b>Security Warning:  </b>Using this function incorrectly can compromise the security of your application. The first argument, <i>psz1</i>, must be large enough to hold <i>psz2</i> and the closing '\0', otherwise a buffer overrun may occur. Buffer overruns may lead to a denial of service attack against the application if an access violation occurs. In the worst case, a buffer overrun may allow an attacker to inject executable code into your process, especially if <i>psz1</i> is a stack-based buffer. Consider using one of the following alternatives: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcata">StringCbCat</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatexa">StringCbCatEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatna">StringCbCatN</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbcatnexa">StringCbCatNEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcata">StringCchCat</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatexa">StringCchCatEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatna">StringCchCatN</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchcatnexa">StringCchCatNEx</a>. You should review <a href="/windows/desktop/shell/sec-shell">Security Considerations: Microsoft Windows Shell</a> before continuing.