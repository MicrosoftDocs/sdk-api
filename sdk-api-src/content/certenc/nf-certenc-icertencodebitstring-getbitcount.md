---
UID: NF:certenc.ICertEncodeBitString.GetBitCount
title: ICertEncodeBitString::GetBitCount (certenc.h)
description: Returns the number of bits in a bit string that belongs to the CertEncodeBitString object and has been initialized by an earlier call to ICertEncodeBitString::Decode.
helpviewer_keywords: ["CCertEncodeBitString object [Security]","GetBitCount method","GetBitCount","GetBitCount method [Security]","GetBitCount method [Security]","CCertEncodeBitString object","GetBitCount method [Security]","ICertEncodeBitString interface","ICertEncodeBitString interface [Security]","GetBitCount method","ICertEncodeBitString.GetBitCount","ICertEncodeBitString::GetBitCount","_certsrv_icertencodebitstring_getbitcount","certenc/ICertEncodeBitString::GetBitCount","security.icertencodebitstring_getbitcount"]
old-location: security\icertencodebitstring_getbitcount.htm
tech.root: security
ms.assetid: 9fbaaf03-02b8-4c6f-8cc2-3fd897fdc81d
ms.date: 12/05/2018
ms.keywords: CCertEncodeBitString object [Security],GetBitCount method, GetBitCount, GetBitCount method [Security], GetBitCount method [Security],CCertEncodeBitString object, GetBitCount method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],GetBitCount method, ICertEncodeBitString.GetBitCount, ICertEncodeBitString::GetBitCount, _certsrv_icertencodebitstring_getbitcount, certenc/ICertEncodeBitString::GetBitCount, security.icertencodebitstring_getbitcount
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
 - ICertEncodeBitString::GetBitCount
 - certenc/ICertEncodeBitString::GetBitCount
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
 - ICertEncodeBitString.GetBitCount
 - CCertEncodeBitString.GetBitCount
---

# ICertEncodeBitString::GetBitCount


## -description

The <b>GetBitCount</b> method returns the number of bits in a bit string that belongs to the 
<a href="/windows/desktop/api/certenc/nn-certenc-icertencodebitstring">CertEncodeBitString</a> object and has been initialized by an earlier call to 
<a href="/windows/desktop/api/certenc/nf-certenc-icertencodebitstring-decode">ICertEncodeBitString::Decode</a>.

## -parameters

### -param pBitCount [out]

A pointer to a <b>Long</b> that will receive the number of bits in the bit string.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of bits in the bit string.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodebitstring">ICertEncodeBitString</a>