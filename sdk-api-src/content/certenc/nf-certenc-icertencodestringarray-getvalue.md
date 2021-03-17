---
UID: NF:certenc.ICertEncodeStringArray.GetValue
title: ICertEncodeStringArray::GetValue (certenc.h)
description: Returns the specified string from the string array.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","GetValue method","GetValue","GetValue method [Security]","GetValue method [Security]","CCertEncodeStringArray object","GetValue method [Security]","ICertEncodeStringArray interface","ICertEncodeStringArray interface [Security]","GetValue method","ICertEncodeStringArray.GetValue","ICertEncodeStringArray::GetValue","_certsrv_icertencodestringarray_getvalue","certenc/ICertEncodeStringArray::GetValue","security.icertencodestringarray_getvalue"]
old-location: security\icertencodestringarray_getvalue.htm
tech.root: security
ms.assetid: 93f827c6-4dc6-462f-8865-eb631d7fe7bc
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],GetValue method, GetValue, GetValue method [Security], GetValue method [Security],CCertEncodeStringArray object, GetValue method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],GetValue method, ICertEncodeStringArray.GetValue, ICertEncodeStringArray::GetValue, _certsrv_icertencodestringarray_getvalue, certenc/ICertEncodeStringArray::GetValue, security.icertencodestringarray_getvalue
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeStringArray::GetValue
 - certenc/ICertEncodeStringArray::GetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeStringArray.GetValue
 - CCertEncodeStringArray.GetValue
---

# ICertEncodeStringArray::GetValue


## -description

The <b>GetValue</b> method returns the specified string from the string array.

## -parameters

### -param Index [in]

The zero-based index that specifies the string to retrieve.

### -param pstr [out]

A pointer to a <b>BSTR</b> that represents the string value. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the string value at the specified index.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-getstringtype">ICertEncodeStringArray::GetStringType</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-setvalue">ICertEncodeStringArray::SetValue</a>