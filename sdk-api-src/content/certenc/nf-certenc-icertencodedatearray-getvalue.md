---
UID: NF:certenc.ICertEncodeDateArray.GetValue
title: ICertEncodeDateArray::GetValue (certenc.h)
description: Returns the specified date from the DATE array.
helpviewer_keywords: ["CCertEncodeDateArray object [Security]","GetValue method","GetValue","GetValue method [Security]","GetValue method [Security]","CCertEncodeDateArray object","GetValue method [Security]","ICertEncodeDateArray interface","ICertEncodeDateArray interface [Security]","GetValue method","ICertEncodeDateArray.GetValue","ICertEncodeDateArray::GetValue","_certsrv_icertencodedatearray_getvalue","certenc/ICertEncodeDateArray::GetValue","security.icertencodedatearray_getvalue"]
old-location: security\icertencodedatearray_getvalue.htm
tech.root: security
ms.assetid: db108b2a-c3ee-4ef8-be5c-74dc739dacee
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],GetValue method, GetValue, GetValue method [Security], GetValue method [Security],CCertEncodeDateArray object, GetValue method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],GetValue method, ICertEncodeDateArray.GetValue, ICertEncodeDateArray::GetValue, _certsrv_icertencodedatearray_getvalue, certenc/ICertEncodeDateArray::GetValue, security.icertencodedatearray_getvalue
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
 - ICertEncodeDateArray::GetValue
 - certenc/ICertEncodeDateArray::GetValue
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
 - ICertEncodeDateArray.GetValue
 - CCertEncodeDateArray.GetValue
---

# ICertEncodeDateArray::GetValue


## -description

The <b>GetValue</b> method returns the specified date from the <b>DATE</b> array.

## -parameters

### -param Index [in]

The zero-based index that specifies the date to retrieve.

### -param pValue [out]

A pointer to a <b>DATE</b> variable that receives the date.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the <b>DATE</b> value at the specified index.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-getcount">ICertEncodeDateArray::GetCount</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-setvalue">ICertEncodeDateArray::SetValue</a>