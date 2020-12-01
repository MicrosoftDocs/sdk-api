---
UID: NF:certenc.ICertEncodeStringArray.GetCount
title: ICertEncodeStringArray::GetCount (certenc.h)
description: Returns the number of string values in the string array.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","GetCount method","GetCount","GetCount method [Security]","GetCount method [Security]","CCertEncodeStringArray object","GetCount method [Security]","ICertEncodeStringArray interface","ICertEncodeStringArray interface [Security]","GetCount method","ICertEncodeStringArray.GetCount","ICertEncodeStringArray::GetCount","_certsrv_icertencodestringarray_getcount","certenc/ICertEncodeStringArray::GetCount","security.icertencodestringarray_getcount"]
old-location: security\icertencodestringarray_getcount.htm
tech.root: security
ms.assetid: c02a23ea-87c2-4458-8b1a-b010e8103a90
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],GetCount method, GetCount, GetCount method [Security], GetCount method [Security],CCertEncodeStringArray object, GetCount method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],GetCount method, ICertEncodeStringArray.GetCount, ICertEncodeStringArray::GetCount, _certsrv_icertencodestringarray_getcount, certenc/ICertEncodeStringArray::GetCount, security.icertencodestringarray_getcount
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
 - ICertEncodeStringArray::GetCount
 - certenc/ICertEncodeStringArray::GetCount
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
 - ICertEncodeStringArray.GetCount
 - CCertEncodeStringArray.GetCount
---

# ICertEncodeStringArray::GetCount


## -description

The <b>GetCount</b> method returns the number of string values in the string array.

## -parameters

### -param pCount [out]

A pointer to a <b>LONG</b> that receives the number of string values contained in the string array.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of string values contained in the string array.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-reset">ICertEncodeStringArray::Reset</a>