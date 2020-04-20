---
UID: NF:wincred.CredFindBestCredentialA
title: CredFindBestCredentialA function (wincred.h)
description: Searches the Credentials Management (CredMan) database for the set of generic credentials that are associated with the current logon session and that best match the specified target resource.helpviewer_keywords: ["CredFindBestCredential","CredFindBestCredential function [Security]","CredFindBestCredentialA","CredFindBestCredentialW","security.credfindbestcredential","wincred/CredFindBestCredential","wincred/CredFindBestCredentialA","wincred/CredFindBestCredentialW"]
old-location: security\credfindbestcredential.htm
tech.root: SecAuthN
ms.assetid: b39e3167-dd63-4b81-b850-f3117be348a5
ms.date: 12/05/2018
ms.keywords: CredFindBestCredential, CredFindBestCredential function [Security], CredFindBestCredentialA, CredFindBestCredentialW, security.credfindbestcredential, wincred/CredFindBestCredential, wincred/CredFindBestCredentialA, wincred/CredFindBestCredentialW
f1_keywords:
- wincred/CredFindBestCredential
dev_langs:
- c++
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredFindBestCredentialW (Unicode) and CredFindBestCredentialA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
- sechost.dll
- API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
- CredFindBestCredential
- CredFindBestCredentialA
- CredFindBestCredentialW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CredFindBestCredentialA function


## -description


The <b>CredFindBestCredential</b> function searches the <a href="https://docs.microsoft.com/windows/desktop/SecAuthN/credentials-management">Credentials Management</a> (CredMan) database for the set of generic credentials that are associated with the current logon session and that best match the specified target resource.


## -parameters




### -param TargetName [in]

A pointer to a null-terminated string that contains the name of the target resource for which to find credentials.


### -param Type [in]

The type of credentials to search for. Currently, this function supports only <b>CRED_TYPE_GENERIC</b>.


### -param Flags [in]

Reserved.


### -param Credential [out]

The address of a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wincred/ns-wincred-credentiala">CREDENTIAL</a> structure that specifies the set of credentials this function finds.

When you have finished using this structure, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincred/nf-wincred-credfree">CredFree</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



