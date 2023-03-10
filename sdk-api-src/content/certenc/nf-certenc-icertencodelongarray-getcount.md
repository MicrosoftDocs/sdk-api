---
UID: NF:certenc.ICertEncodeLongArray.GetCount
title: ICertEncodeLongArray::GetCount (certenc.h)
description: Returns the number of Long values in the object's Long array.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","GetCount method","GetCount","GetCount method [Security]","GetCount method [Security]","CCertEncodeLongArray object","GetCount method [Security]","ICertEncodeLongArray interface","ICertEncodeLongArray interface [Security]","GetCount method","ICertEncodeLongArray.GetCount","ICertEncodeLongArray::GetCount","_certsrv_icertencodelongarray_getcount","certenc/ICertEncodeLongArray::GetCount","security.icertencodelongarray_getcount"]
old-location: security\icertencodelongarray_getcount.htm
tech.root: security
ms.assetid: f60cffb1-5202-4dc8-97dd-9eddd381602a
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeLongArray object, GetCount method [Security],ICertEncodeLongArray interface, ICertEncodeLongArray interface [Security],GetCount method, ICertEncodeLongArray.GetCount, ICertEncodeLongArray::GetCount, _certsrv_icertencodelongarray_getcount, certenc/ICertEncodeLongArray::GetCount, security.icertencodelongarray_getcount
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
 - ICertEncodeLongArray::GetCount
 - certenc/ICertEncodeLongArray::GetCount
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
 - ICertEncodeLongArray.GetCount
 - CCertEncodeLongArray.GetCount
---

# ICertEncodeLongArray::GetCount


## -description

The <b>GetCount</b> method returns the number of <b>Long</b> values in the object's <b>Long</b> array.

## -parameters

### -param pCount [out]

A pointer to a <b>Long</b> that receives the number of <b>Long</b> values contained in the <b>Long</b> array.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is the number of <b>Long</b> values contained in the <b>Long</b> array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-reset">ICertEncodeLongArray::Reset</a>