---
UID: NF:certenc.ICertEncodeLongArray.Reset
title: ICertEncodeLongArray::Reset (certenc.h)
description: Specifies the size of the array in this object.
helpviewer_keywords: ["CCertEncodeLongArray object [Security]","Reset method","ICertEncodeLongArray interface [Security]","Reset method","ICertEncodeLongArray.Reset","ICertEncodeLongArray::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertEncodeLongArray object","Reset method [Security]","ICertEncodeLongArray interface","_certsrv_icertencodelongarray_reset","certenc/ICertEncodeLongArray::Reset","security.icertencodelongarray_reset"]
old-location: security\icertencodelongarray_reset.htm
tech.root: security
ms.assetid: 4b5821e0-c81a-47b7-98b0-2a293967d8f6
ms.date: 12/05/2018
ms.keywords: CCertEncodeLongArray object [Security],Reset method, ICertEncodeLongArray interface [Security],Reset method, ICertEncodeLongArray.Reset, ICertEncodeLongArray::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeLongArray object, Reset method [Security],ICertEncodeLongArray interface, _certsrv_icertencodelongarray_reset, certenc/ICertEncodeLongArray::Reset, security.icertencodelongarray_reset
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
 - ICertEncodeLongArray::Reset
 - certenc/ICertEncodeLongArray::Reset
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
 - ICertEncodeLongArray.Reset
 - CCertEncodeLongArray.Reset
---

# ICertEncodeLongArray::Reset


## -description

The <b>Reset</b> method specifies the size of the array in this object. The values of all the elements in the array are set to zero.
		You must call this method before calling the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodelongarray-setvalue">ICertEncodeLongArray::SetValue</a> method for the first time.

## -parameters

### -param Count [in]

Specifies the number of elements in the <b>Long</b> array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodelongarray">ICertEncodeLongArray</a>