---
UID: NF:certenc.ICertEncodeDateArray.GetCount
title: ICertEncodeDateArray::GetCount (certenc.h)
description: Returns the number of DATE values in the object's DATE array.
helpviewer_keywords: ["CCertEncodeDateArray object [Security]","GetCount method","GetCount","GetCount method [Security]","GetCount method [Security]","CCertEncodeDateArray object","GetCount method [Security]","ICertEncodeDateArray interface","ICertEncodeDateArray interface [Security]","GetCount method","ICertEncodeDateArray.GetCount","ICertEncodeDateArray::GetCount","_certsrv_icertencodedatearray_getcount","certenc/ICertEncodeDateArray::GetCount","security.icertencodedatearray_getcount"]
old-location: security\icertencodedatearray_getcount.htm
tech.root: security
ms.assetid: 25c61f42-b190-44c3-b2ba-57861bdfbce3
ms.date: 12/05/2018
ms.keywords: CCertEncodeDateArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeDateArray object, GetCount method [Security],ICertEncodeDateArray interface, ICertEncodeDateArray interface [Security],GetCount method, ICertEncodeDateArray.GetCount, ICertEncodeDateArray::GetCount, _certsrv_icertencodedatearray_getcount, certenc/ICertEncodeDateArray::GetCount, security.icertencodedatearray_getcount
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
 - ICertEncodeDateArray::GetCount
 - certenc/ICertEncodeDateArray::GetCount
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
 - ICertEncodeDateArray.GetCount
 - CCertEncodeDateArray.GetCount
---

# ICertEncodeDateArray::GetCount


## -description

The <b>GetCount</b> method returns the number of <b>DATE</b> values in the object's <b>DATE</b> array.

## -parameters

### -param pCount [out]

A pointer to a <b>LONG</b> that receives the number of <b>DATE</b> values contained in the <b>DATE</b> array.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of <b>DATE</b> values contained in the <b>DATE</b> array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodedatearray">ICertEncodeDateArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-getvalue">ICertEncodeDateArray::GetValue</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodedatearray-reset">ICertEncodeDateArray::Reset</a>