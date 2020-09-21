---
UID: NF:certenc.ICertEncodeDateArray.Reset
title: ICertEncodeDateArray::Reset (certenc.h)
description: Specifies the size of DATE array in this object.
helpviewer_keywords: ["CCertEncodeDateArray object [Security]","Reset method","ICertEncodeDateArray interface [Security]","Reset method","ICertEncodeDateArray.Reset","ICertEncodeDateArray::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertEncodeDateArray object","Reset method [Security]","ICertEncodeDateArray interface","_certsrv_icertencodedatearray_reset","certenc/ICertEncodeDateArray::Reset","security.icertencodedatearray_reset"]
old-location: security\icertencodedatearray_reset.htm
tech.root: security
ms.assetid: f09087aa-ae10-4a59-9b59-5f8b72254ce6
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],Reset method, ICertEncodeDateArray interface [Security],Reset method, ICertEncodeDateArray.Reset, ICertEncodeDateArray::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeDateArray object, Reset method [Security],ICertEncodeDateArray interface, _certsrv_icertencodedatearray_reset, certenc/ICertEncodeDateArray::Reset, security.icertencodedatearray_reset
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
 - ICertEncodeDateArray::Reset
 - certenc/ICertEncodeDateArray::Reset
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
 - ICertEncodeDateArray.Reset
 - CCertEncodeDateArray.Reset
---

# ICertEncodeDateArray::Reset


## -description

The <b>Reset</b> method specifies the size of <b>DATE</b> array in this object. The values of all the elements in the array are set to zero. You must call this method before calling the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-setvalue">ICertEncodeDateArray::SetValue</a> method for the first time.

## -parameters

### -param Count [in]

Specifies the number of elements in the <b>DATE</b> array.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-setvalue">ICertEncodeDateArray::SetValue</a>