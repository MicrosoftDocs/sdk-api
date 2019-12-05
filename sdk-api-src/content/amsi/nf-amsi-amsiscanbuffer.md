---
UID: NF:amsi.AmsiScanBuffer
title: AmsiScanBuffer function (amsi.h)
description: Scans a buffer-full of content for malware.
old-location: amsi\amsiscanbuffer.htm
tech.root: AMSI
ms.assetid: D1F2EBE7-FD6B-4CD4-BE4F-F536F08EE339
ms.date: 12/05/2018
ms.keywords: AmsiScanBuffer, AmsiScanBuffer function [Antimalware Scan Interface], amsi.amsiscanbuffer, amsi/AmsiScanBuffer
ms.topic: function
f1_keywords:
- amsi/AmsiScanBuffer
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- amsi.dll
api_name:
- AmsiScanBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AmsiScanBuffer function


## -description


Scans a buffer-full of content for malware.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.


### -param buffer [in]

The buffer from which to read the data to be scanned.


### -param length [in]

The length, in bytes, of the data to be read from <i>buffer</i>.


### -param contentName [in]

The filename, URL, unique script ID, or similar of the content being scanned.


### -param amsiSession [in, optional]

If multiple scan requests are to be correlated within a session, set <i>session</i> to the handle of type HAMSISESSION that was initially received from <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>. Otherwise, set <i>session</i> to <b>nullptr</b>.


### -param result [out]

The result of the scan. See <a href="https://docs.microsoft.com/windows/desktop/api/amsi/ne-amsi-amsi_result">AMSI_RESULT</a>.

An app should use <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiresultismalware">AmsiResultIsMalware</a> to determine whether the content should be blocked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amsi/ne-amsi-amsi_result">AMSI_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiresultismalware">AmsiResultIsMalware</a>
 

 

