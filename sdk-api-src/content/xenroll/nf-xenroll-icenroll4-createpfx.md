---
UID: NF:xenroll.ICEnroll4.createPFX
title: ICEnroll4::createPFX (xenroll.h)
description: Saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS (ICEnroll4.createPFX)
helpviewer_keywords: ["CEnroll object [Security]","createPFX method","ICEnroll4 interface [Security]","createPFX method","ICEnroll4.createPFX","ICEnroll4::createPFX","_xen_icenroll4_createpfx","createPFX","createPFX method [Security]","createPFX method [Security]","CEnroll object","createPFX method [Security]","ICEnroll4 interface","security.icenroll4_createpfx","xenroll/ICEnroll4::createPFX"]
old-location: security\icenroll4_createpfx.htm
tech.root: security
ms.assetid: 37b69fc6-db16-4491-b596-4ef76e5414b3
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createPFX method, ICEnroll4 interface [Security],createPFX method, ICEnroll4.createPFX, ICEnroll4::createPFX, _xen_icenroll4_createpfx, createPFX, createPFX method [Security], createPFX method [Security],CEnroll object, createPFX method [Security],ICEnroll4 interface, security.icenroll4_createpfx, xenroll/ICEnroll4::createPFX
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
 - ICEnroll4::createPFX
 - xenroll/ICEnroll4::createPFX
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
 - ICEnroll4.createPFX
 - CEnroll.createPFX
---

# ICEnroll4::createPFX


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPFX</b> method saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS #12.
			
This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param strPassword [in]

A password for the PFX-format message. This value can be empty or <b>NULL</b> to indicate that no password is used.  When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param pstrPFX [out]

A pointer to a <b>BSTR</b> that receives the base64-encoded PFX format certificate information. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains the PFX format certificate information.

## -remarks

This method is disabled when  the Certificate Enrollment Control is executed as a scripted control.
