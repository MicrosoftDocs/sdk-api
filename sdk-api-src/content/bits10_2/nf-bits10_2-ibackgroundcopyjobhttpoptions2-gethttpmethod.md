---
UID: NF:bits10_2.IBackgroundCopyJobHttpOptions2.GetHttpMethod
title: IBackgroundCopyJobHttpOptions2::GetHttpMethod (bits10_2.h)
description: Retrieves a wide string containing the HTTP method name for the BITS transfer. By default, download jobs will be &quot;GET&quot;, and upload and upload-reply jobs will be &quot;BITS_POST&quot;.
helpviewer_keywords: ["GetHttpMethod","GetHttpMethod method [BITS]","GetHttpMethod method [BITS]","IBackgroundCopyJobHttpOptions2 interface","IBackgroundCopyJobHttpOptions2 interface [BITS]","GetHttpMethod method","IBackgroundCopyJobHttpOptions2.GetHttpMethod","IBackgroundCopyJobHttpOptions2::GetHttpMethod","bits.ibackgroundcopyjobhttpoptions2_gethttpmethod","bits10_2/IBackgroundCopyJobHttpOptions2::GetHttpMethod"]
old-location: bits\ibackgroundcopyjobhttpoptions2_gethttpmethod.htm
tech.root: Bits
ms.assetid: B855F1A5-AAFC-4E59-8F1D-ABA0034AFDF8
ms.date: 12/05/2018
ms.keywords: GetHttpMethod, GetHttpMethod method [BITS], GetHttpMethod method [BITS],IBackgroundCopyJobHttpOptions2 interface, IBackgroundCopyJobHttpOptions2 interface [BITS],GetHttpMethod method, IBackgroundCopyJobHttpOptions2.GetHttpMethod, IBackgroundCopyJobHttpOptions2::GetHttpMethod, bits.ibackgroundcopyjobhttpoptions2_gethttpmethod, bits10_2/IBackgroundCopyJobHttpOptions2::GetHttpMethod
req.header: bits10_2.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJobHttpOptions2::GetHttpMethod
 - bits10_2/IBackgroundCopyJobHttpOptions2::GetHttpMethod
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJobHttpOptions2.GetHttpMethod
---

# IBackgroundCopyJobHttpOptions2::GetHttpMethod


## -description

Retrieves a wide string containing the HTTP method name for the BITS transfer. By default, download jobs will be "GET", and upload and upload-reply jobs will be "BITS_POST".

## -parameters

### -param method [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The address of a pointer to a null-terminated string of wide characters. If successful, the method updates the pointer to point to a string containing the HTTP method name. When you're done with this string, free it with a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2">IBackgroundCopyJobHttpOptions2</a>
