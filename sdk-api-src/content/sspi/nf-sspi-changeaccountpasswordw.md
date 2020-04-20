---
UID: NF:sspi.ChangeAccountPasswordW
title: ChangeAccountPasswordW function (sspi.h)
description: Changes the password for a Windows domain account by using the specified Security Support Provider.helpviewer_keywords: ["ChangeAccountPassword","ChangeAccountPassword function [Security]","ChangeAccountPasswordA","ChangeAccountPasswordW","security.changeaccountpassword","sspi/ChangeAccountPassword","sspi/ChangeAccountPasswordA","sspi/ChangeAccountPasswordW"]
old-location: security\changeaccountpassword.htm
tech.root: SecAuthN
ms.assetid: a1d1e315-d1a2-499a-b552-83180508271f
ms.date: 12/05/2018
ms.keywords: ChangeAccountPassword, ChangeAccountPassword function [Security], ChangeAccountPasswordA, ChangeAccountPasswordW, security.changeaccountpassword, sspi/ChangeAccountPassword, sspi/ChangeAccountPasswordA, sspi/ChangeAccountPasswordW
f1_keywords:
- sspi/ChangeAccountPassword
dev_langs:
- c++
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ChangeAccountPasswordW (Unicode) and ChangeAccountPasswordA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Secur32.dll
api_name:
- ChangeAccountPassword
- ChangeAccountPasswordA
- ChangeAccountPasswordW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ChangeAccountPasswordW function


## -description


The <b>ChangeAccountPassword</b> function changes the password for a Windows domain account by using the specified <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/sspi">Security Support Provider</a>.

This function is supported only by the <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/microsoft-kerberos">Microsoft Kerberos</a>, <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/microsoft-negotiate">Microsoft Negotiate</a>, and <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/microsoft-ntlm">Microsoft NTLM</a> providers.


## -parameters




### -param pszPackageName [in]

The name of the provider to use. The value of this parameter must be either "Kerberos", "Negotiate", or "NTLM".


### -param pszDomainName [in]

The domain of the account for which to change the password.


### -param pszAccountName [in]

The user name of the account for which to change the password.


### -param pszOldPassword [in]

The old password to be changed.


### -param pszNewPassword [in]

The new password for the specified account.


### -param bImpersonating [in]

<b>TRUE</b> if the calling process is running as the client; otherwise, <b>FALSE</b>.


### -param dwReserved [in]

Reserved. Must be set to zero.


### -param pOutput [in, out]

On input, a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure. The <b>SecBufferDesc</b> structure must contain a single buffer of type <b>SECBUFFER_CHANGE_PASS_RESPONSE</b>. On output, the <b>pvBuffer</b> member of that structure points to a <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-domain_password_information">DOMAIN_PASSWORD_INFORMATION</a> structure.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns an error code.



