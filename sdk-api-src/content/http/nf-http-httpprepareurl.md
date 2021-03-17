---
UID: NF:http.HttpPrepareUrl
title: HttpPrepareUrl function (http.h)
description: Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.
helpviewer_keywords: ["HttpPrepareUrl","HttpPrepareUrl function [HTTP]","http.httpprepareurl","http/HttpPrepareUrl"]
old-location: http\httpprepareurl.htm
tech.root: http
ms.assetid: 45199AEE-950D-44C4-8590-96077DBDC846
ms.date: 12/05/2018
ms.keywords: HttpPrepareUrl, HttpPrepareUrl function [HTTP], http.httpprepareurl, http/HttpPrepareUrl
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpPrepareUrl
 - http/HttpPrepareUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpPrepareUrl
---

# HttpPrepareUrl function


## -description

The <b>HttpPrepareUrl</b> function parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.

## -parameters

### -param Reserved

Reserved.  Must be <b>NULL</b>.

### -param Flags

Reserved. Must be zero.

### -param Url [in]

A pointer to a string that represents the non-normalized Unicode or punycode URL to prepare.

### -param PreparedUrl [out]

On successful output, a pointer to a string that represents the normalized URL.

<div class="alert"><b>Note</b>  Free <i>PreparedUrl</i> using <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>.</div>
<div> </div>

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.