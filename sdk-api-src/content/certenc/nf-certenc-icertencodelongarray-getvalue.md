---
UID: NF:certenc.ICertEncodeLongArray.GetValue
title: ICertEncodeLongArray::GetValue (certenc.h)
description: Returns the specified Long value from the Long array.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","GetValue method","GetValue","GetValue method [Security]","GetValue method [Security]","CCertEncodeLongArray object","GetValue method [Security]","ICertEncodeLongArray interface","ICertEncodeLongArray interface [Security]","GetValue method","ICertEncodeLongArray.GetValue","ICertEncodeLongArray::GetValue","_certsrv_icertencodelongarray_getvalue","certenc/ICertEncodeLongArray::GetValue","security.icertencodelongarray_getvalue"]
old-location: security\icertencodelongarray_getvalue.htm
tech.root: security
ms.assetid: 0a7c1d6b-8fe7-4cc0-8cbd-2831dd3a178b
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],GetValue method, GetValue, GetValue method [Security], GetValue method [Security],CCertEncodeLongArray object, GetValue method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],GetValue method, ICertEncodeLongArray.GetValue, ICertEncodeLongArray::GetValue, _certsrv_icertencodelongarray_getvalue, certenc/ICertEncodeLongArray::GetValue, security.icertencodelongarray_getvalue
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
 - ICertEncodeLongArray::GetValue
 - certenc/ICertEncodeLongArray::GetValue
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
 - ICertEncodeLongArray.GetValue
 - CCertEncodeLongArray.GetValue
---

# ICertEncodeLongArray::GetValue


## -description

The <b>GetValue</b> method returns the specified <b>Long</b> value from the  <b>Long</b> array.

## -parameters

### -param Index [in]

The zero-based index that specifies the <b>Long</b> value to retrieve.

### -param pValue [out]

A pointer to a <b>Long</b> variable that receives the value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the <b>Long</b> value at the specified index.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-setvalue">ICertEncodeLongArray::SetValue</a>