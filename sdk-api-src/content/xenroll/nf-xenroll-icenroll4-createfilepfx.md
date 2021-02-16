---
UID: NF:xenroll.ICEnroll4.createFilePFX
title: ICEnroll4::createFilePFX (xenroll.h)
description: Saves the accepted certificate chain and private key in a file in Personal Information Exchange (PFX) format. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","createFilePFX method","ICEnroll4 interface [Security]","createFilePFX method","ICEnroll4.createFilePFX","ICEnroll4::createFilePFX","_xen_icenroll4_createfilepfx","createFilePFX","createFilePFX method [Security]","createFilePFX method [Security]","CEnroll object","createFilePFX method [Security]","ICEnroll4 interface","security.icenroll4_createfilepfx","xenroll/ICEnroll4::createFilePFX"]
old-location: security\icenroll4_createfilepfx.htm
tech.root: security
ms.assetid: df58ba41-5301-48dd-9255-7173bb73965c
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],createFilePFX method, ICEnroll4 interface [Security],createFilePFX method, ICEnroll4.createFilePFX, ICEnroll4::createFilePFX, _xen_icenroll4_createfilepfx, createFilePFX, createFilePFX method [Security], createFilePFX method [Security],CEnroll object, createFilePFX method [Security],ICEnroll4 interface, security.icenroll4_createfilepfx, xenroll/ICEnroll4::createFilePFX
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
 - ICEnroll4::createFilePFX
 - xenroll/ICEnroll4::createFilePFX
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
 - ICEnroll4.createFilePFX
 - CEnroll.createFilePFX
---

# ICEnroll4::createFilePFX


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePFX</b> method saves the accepted certificate chain and <a href="/windows/desktop/SecGloss/p-gly">private key</a> in a file in Personal Information Exchange (PFX) format. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param strPassword [in]

A password for the PFX; this value can be empty (or <b>NULL</b>) to indicate that no password is used. When you have finished using the password, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function.  For more information about handling passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param strPFXFileName [in]

The name of the file that will receive the base64-encoded PFX data.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When this method is called from script, the method displays a user interface that asks whether the user will allow a write operation to the file system.