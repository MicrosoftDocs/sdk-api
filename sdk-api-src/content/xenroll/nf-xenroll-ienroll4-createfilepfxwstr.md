---
UID: NF:xenroll.IEnroll4.createFilePFXWStr
title: IEnroll4::createFilePFXWStr (xenroll.h)
description: Saves the accepted certificate chain and private key in a file in Personal Information Exchange (PFX) format.
helpviewer_keywords: ["IEnroll4 interface [Security]","createFilePFXWStr method","IEnroll4.createFilePFXWStr","IEnroll4::createFilePFXWStr","createFilePFXWStr","createFilePFXWStr method [Security]","createFilePFXWStr method [Security]","IEnroll4 interface","security.ienroll4_createfilepfxwstr","xenroll/IEnroll4::createFilePFXWStr"]
old-location: security\ienroll4_createfilepfxwstr.htm
tech.root: security
ms.assetid: 1df364e7-35ab-4c16-ac13-2f0be36fe0f9
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],createFilePFXWStr method, IEnroll4.createFilePFXWStr, IEnroll4::createFilePFXWStr, createFilePFXWStr, createFilePFXWStr method [Security], createFilePFXWStr method [Security],IEnroll4 interface, security.ienroll4_createfilepfxwstr, xenroll/IEnroll4::createFilePFXWStr
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
 - IEnroll4::createFilePFXWStr
 - xenroll/IEnroll4::createFilePFXWStr
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
 - IEnroll4.createFilePFXWStr
---

# IEnroll4::createFilePFXWStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePFXWStr</b> method saves the accepted certificate chain and <a href="/windows/desktop/SecGloss/p-gly">private key</a> in a file in Personal Information Exchange (PFX) format. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pwszPassword [in]

A pointer to a <b>null</b>-terminated wide character string that represents the password for the PFX-format message. This value may be empty or <b>NULL</b> to indicate that no password is used. When you have finished using the password, remove the sensitive information from memory by calling <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a>. For more information about protecting the password, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param pwszPFXFileName [in]

A pointer to a <b>null</b>-terminated wide character string that contains the name of the file that will receive the base64-encoded PFX data.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>