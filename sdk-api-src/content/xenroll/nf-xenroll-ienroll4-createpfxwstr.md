---
UID: NF:xenroll.IEnroll4.createPFXWStr
title: IEnroll4::createPFXWStr (xenroll.h)
description: Saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS (IEnroll4.createPFXWStr)
helpviewer_keywords: ["IEnroll4 interface [Security]","createPFXWStr method","IEnroll4.createPFXWStr","IEnroll4::createPFXWStr","createPFXWStr","createPFXWStr method [Security]","createPFXWStr method [Security]","IEnroll4 interface","security.ienroll4_createpfxwstr","xenroll/IEnroll4::createPFXWStr"]
old-location: security\ienroll4_createpfxwstr.htm
tech.root: security
ms.assetid: 38ab5b07-2a84-484b-b413-58f0e11599e9
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],createPFXWStr method, IEnroll4.createPFXWStr, IEnroll4::createPFXWStr, createPFXWStr, createPFXWStr method [Security], createPFXWStr method [Security],IEnroll4 interface, security.ienroll4_createpfxwstr, xenroll/IEnroll4::createPFXWStr
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
 - IEnroll4::createPFXWStr
 - xenroll/IEnroll4::createPFXWStr
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
 - IEnroll4.createPFXWStr
---

# IEnroll4::createPFXWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPFXWStr</b> method saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS #12. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pwszPassword [in]

A pointer to a null-terminated Unicode string that represents the password for the PFX-format message. This value may be empty or <b>NULL</b> to indicate that no password is used. When you have finished using the password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param pblobPFX [out]

A pointer to the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure  that receives the base64-encoded PFX format certificate information.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
