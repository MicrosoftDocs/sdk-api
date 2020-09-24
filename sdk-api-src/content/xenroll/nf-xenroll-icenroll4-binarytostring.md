---
UID: NF:xenroll.ICEnroll4.binaryToString
title: ICEnroll4::binaryToString (xenroll.h)
description: Converts a binary data BLOB to a string. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","binaryToString method","ICEnroll4 interface [Security]","binaryToString method","ICEnroll4.binaryToString","ICEnroll4::binaryToString","_xen_icenroll4_binarytostring","binaryToString","binaryToString method [Security]","binaryToString method [Security]","CEnroll object","binaryToString method [Security]","ICEnroll4 interface","security.icenroll4_binarytostring","xenroll/ICEnroll4::binaryToString"]
old-location: security\icenroll4_binarytostring.htm
tech.root: security
ms.assetid: 43358d84-ccdd-49a8-be1d-bb5e8ddd1397
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],binaryToString method, ICEnroll4 interface [Security],binaryToString method, ICEnroll4.binaryToString, ICEnroll4::binaryToString, _xen_icenroll4_binarytostring, binaryToString, binaryToString method [Security], binaryToString method [Security],CEnroll object, binaryToString method [Security],ICEnroll4 interface, security.icenroll4_binarytostring, xenroll/ICEnroll4::binaryToString
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::binaryToString
 - xenroll/ICEnroll4::binaryToString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.binaryToString
 - CEnroll.binaryToString
---

# ICEnroll4::binaryToString


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>binaryToString</b> method converts a binary data <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> to a string. 
			This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

This method uses the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a> function to do the conversion.

## -parameters

### -param Flags [in]

The value passed to the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a> function. For a description of possible values, see 
<b>CryptBinaryToString</b>.

### -param strBinary [in]

A binary data BLOB to be converted to a string.

### -param pstrEncoded [out]

A pointer to a <b>BSTR</b> that receives the encoded data. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that represents the binary data.