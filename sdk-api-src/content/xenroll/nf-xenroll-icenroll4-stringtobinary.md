---
UID: NF:xenroll.ICEnroll4.stringToBinary
title: ICEnroll4::stringToBinary (xenroll.h)
description: Converts an encoded string to a binary data BLOB. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","stringToBinary method","ICEnroll4 interface [Security]","stringToBinary method","ICEnroll4.stringToBinary","ICEnroll4::stringToBinary","_xen_icenroll4_stringtobinary","security.icenroll4_stringtobinary","stringToBinary","stringToBinary method [Security]","stringToBinary method [Security]","CEnroll object","stringToBinary method [Security]","ICEnroll4 interface","xenroll/ICEnroll4::stringToBinary"]
old-location: security\icenroll4_stringtobinary.htm
tech.root: security
ms.assetid: abcc395f-f989-4098-818a-160e427b1da0
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],stringToBinary method, ICEnroll4 interface [Security],stringToBinary method, ICEnroll4.stringToBinary, ICEnroll4::stringToBinary, _xen_icenroll4_stringtobinary, security.icenroll4_stringtobinary, stringToBinary, stringToBinary method [Security], stringToBinary method [Security],CEnroll object, stringToBinary method [Security],ICEnroll4 interface, xenroll/ICEnroll4::stringToBinary
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
 - ICEnroll4::stringToBinary
 - xenroll/ICEnroll4::stringToBinary
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
 - ICEnroll4.stringToBinary
 - CEnroll.stringToBinary
---

# ICEnroll4::stringToBinary


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>stringToBinary</b> method converts an encoded string to a binary data <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

The <b>stringToBinary</b> method calls the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptstringtobinarya">CryptStringToBinary</a> function.

## -parameters

### -param Flags [in]

A value passed to the <i>dwFlags</i> parameter of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptstringtobinarya">CryptStringToBinary</a> function. For valid values, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptstringtobinarya">CryptStringToBinary</a>.

### -param strEncoded [in]

An encoded string to be converted to a binary data <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

### -param pstrBinary [out]

A pointer to a  <b>BSTR</b> that receives the binary data. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that contains the binary data.