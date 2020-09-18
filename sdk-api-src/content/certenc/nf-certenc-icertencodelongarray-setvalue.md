---
UID: NF:certenc.ICertEncodeLongArray.SetValue
title: ICertEncodeLongArray::SetValue (certenc.h)
description: Sets a Long value at the specified index of the Long array.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","SetValue method","ICertEncodeLongArray interface [Security]","SetValue method","ICertEncodeLongArray.SetValue","ICertEncodeLongArray::SetValue","SetValue","SetValue method [Security]","SetValue method [Security]","CCertEncodeLongArray object","SetValue method [Security]","ICertEncodeLongArray interface","_certsrv_icertencodelongarray_setvalue","certenc/ICertEncodeLongArray::SetValue","security.icertencodelongarray_setvalue"]
old-location: security\icertencodelongarray_setvalue.htm
tech.root: security
ms.assetid: 021b2539-3226-4893-af76-9b7b1637e12e
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],SetValue method, ICertEncodeLongArray interface [Security],SetValue method, ICertEncodeLongArray.SetValue, ICertEncodeLongArray::SetValue, SetValue, SetValue method [Security], SetValue method [Security],CCertEncodeLongArray object, SetValue method [Security],ICertEncodeLongArray interface, _certsrv_icertencodelongarray_setvalue, certenc/ICertEncodeLongArray::SetValue, security.icertencodelongarray_setvalue
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
 - ICertEncodeLongArray::SetValue
 - certenc/ICertEncodeLongArray::SetValue
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
 - ICertEncodeLongArray.SetValue
 - CCertEncodeLongArray.SetValue
---

# ICertEncodeLongArray::SetValue


## -description

The <b>SetValue</b> method sets a <b>Long</b> value at the specified index of the <b>Long</b> array.

 You must call 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">ICertEncodeLongArray::Reset</a> before calling <b>SetValue</b> for the first time.

## -parameters

### -param Index [in]

The zero-based index that specifies the index of the array element to set.

### -param Value [in]

Specifies the <b>Long</b> value to set.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-getvalue">ICertEncodeLongArray::GetValue</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">ICertEncodeLongArray::Reset</a>