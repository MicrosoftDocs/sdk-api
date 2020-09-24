---
UID: NF:certenc.ICertEncodeBitString.GetBitString
title: ICertEncodeBitString::GetBitString (certenc.h)
description: Returns the string of bits in the object's bit string.
helpviewer_keywords: ["CCertEncodeBitString object [Security]","GetBitString method","GetBitString","GetBitString method [Security]","GetBitString method [Security]","CCertEncodeBitString object","GetBitString method [Security]","ICertEncodeBitString interface","ICertEncodeBitString interface [Security]","GetBitString method","ICertEncodeBitString.GetBitString","ICertEncodeBitString::GetBitString","_certsrv_icertencodebitstring_getbitstring","certenc/ICertEncodeBitString::GetBitString","security.icertencodebitstring_getbitstring"]
old-location: security\icertencodebitstring_getbitstring.htm
tech.root: security
ms.assetid: d0c6c501-3aaa-42ab-a077-69f6d24f1eff
ms.date: 12/05/2018
ms.keywords: CCertEncodeBitString object [Security],GetBitString method, GetBitString, GetBitString method [Security], GetBitString method [Security],CCertEncodeBitString object, GetBitString method [Security],ICertEncodeBitString interface, ICertEncodeBitString interface [Security],GetBitString method, ICertEncodeBitString.GetBitString, ICertEncodeBitString::GetBitString, _certsrv_icertencodebitstring_getbitstring, certenc/ICertEncodeBitString::GetBitString, security.icertencodebitstring_getbitstring
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
 - ICertEncodeBitString::GetBitString
 - certenc/ICertEncodeBitString::GetBitString
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
 - ICertEncodeBitString.GetBitString
 - CCertEncodeBitString.GetBitString
---

# ICertEncodeBitString::GetBitString


## -description

The <b>GetBitString</b> method returns the string of bits in the object's bit string.

## -parameters

### -param pstrBitString [out]

A pointer to a <b>BSTR</b> that will contain the bit string. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the bit string.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodebitstring">ICertEncodeBitString</a>