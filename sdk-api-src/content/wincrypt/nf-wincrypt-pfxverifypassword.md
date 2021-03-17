---
UID: NF:wincrypt.PFXVerifyPassword
title: PFXVerifyPassword function (wincrypt.h)
description: The PFXVerifyPassword function attempts to decode the outer layer of a BLOB as a Personal Information Exchange (PFX) packet and to decrypt it with the given password. No data from the BLOB is imported.
helpviewer_keywords: ["PFXVerifyPassword","PFXVerifyPassword function [Security]","_crypto2_pfxverifypassword","security.pfxverifypassword","wincrypt/PFXVerifyPassword"]
old-location: security\pfxverifypassword.htm
tech.root: security
ms.assetid: 47560192-547e-4440-9f10-43327355e1a0
ms.date: 12/05/2018
ms.keywords: PFXVerifyPassword, PFXVerifyPassword function [Security], _crypto2_pfxverifypassword, security.pfxverifypassword, wincrypt/PFXVerifyPassword
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFXVerifyPassword
 - wincrypt/PFXVerifyPassword
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - PFXVerifyPassword
---

# PFXVerifyPassword function


## -description

The <b>PFXVerifyPassword</b> function attempts to decode the outer layer of a BLOB as a Personal Information Exchange (PFX) packet and to decrypt it with the given password. No data from the BLOB is imported.

The PFX format is also known as the Public-Key Cryptography Standards #12 (PKCS #12) format.

## -parameters

### -param pPFX [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that the function will attempt to decode as a PFX packet.

### -param szPassword [in]

String password to be checked. For this function to succeed, this password must be exactly the same as the password used to encrypt the packet.

If you set this value to an empty string or <b>NULL</b>, this function typically attempts to decrypt the password embedded in the PFX BLOB by using the empty string or <b>NULL</b>.

However, beginning with Windows 8 and Windows Server 2012, if a <b>NULL</b> or empty password was specified when the PFX BLOB was created and the application also specified  that the password should be protected to an Active Directory (AD) principal, the Cryptography API (CAPI) randomly generates a password, encrypts it to the AD principal and embeds it in the PFX BLOB. The <b>PFXVerifyPassword</b> function will then try to use the specified AD principal (current user, computer, or AD group member) to decrypt the password. For more information about protecting PFX to an AD principal, see the <i>pvPara</i> parameter and the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function.

When you have finished using the password, clear the password from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param dwFlags [in]

Reserved for future use.

## -returns

The function return <b>TRUE</b> if the password appears correct; otherwise, it returns <b>FALSE</b>.