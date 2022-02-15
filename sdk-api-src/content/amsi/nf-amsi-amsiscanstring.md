---
UID: NF:amsi.AmsiScanString
title: AmsiScanString function (amsi.h)
description: Scans a string for malware.
helpviewer_keywords: ["AmsiScanString","AmsiScanString function [Antimalware Scan Interface]","amsi.amsiscanstring","amsi/AmsiScanString"]
old-location: amsi\amsiscanstring.htm
tech.root: AMSI
ms.assetid: 7D26C57B-014B-4506-A29D-33699808B111
ms.date: 12/05/2018
ms.keywords: AmsiScanString, AmsiScanString function [Antimalware Scan Interface], amsi.amsiscanstring, amsi/AmsiScanString
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AmsiScanString
 - amsi/AmsiScanString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiScanString
---

# AmsiScanString function


## -description

Scans a string for malware.

## -parameters

### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.

### -param string [in]

The string to be scanned.

### -param contentName [in]

The filename, URL, unique script ID, or similar of the content being scanned.

### -param amsiSession [in, optional]

If multiple scan requests are to be correlated within a session, set <i>session</i> to the handle of type HAMSISESSION that was initially received from <a href="/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>. Otherwise, set <i>session</i> to <b>nullptr</b>.

### -param result [out]

The result of the scan. See <a href="/windows/desktop/api/amsi/ne-amsi-amsi_result">AMSI_RESULT</a>.

An app should use <a href="/windows/desktop/api/amsi/nf-amsi-amsiresultismalware">AmsiResultIsMalware</a> to determine whether the content should be blocked.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/amsi/ne-amsi-amsi_result">AMSI_RESULT</a>



<a href="/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>



<a href="/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>



<a href="/windows/desktop/api/amsi/nf-amsi-amsiresultismalware">AmsiResultIsMalware</a>