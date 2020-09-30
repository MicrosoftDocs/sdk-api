---
UID: NF:wincred.CredUIStoreSSOCredW
title: CredUIStoreSSOCredW function (wincred.h)
description: The CredUIStoreSSOCredW function stores a single logon credential.
helpviewer_keywords: ["CredUIStoreSSOCredW","CredUIStoreSSOCredW function [Security]","security.creduistoressocredw","wincred/CredUIStoreSSOCredW"]
old-location: security\creduistoressocredw.htm
tech.root: security
ms.assetid: 2c57c943-bcf7-405c-be0a-a3d1991f3004
ms.date: 12/05/2018
ms.keywords: CredUIStoreSSOCredW, CredUIStoreSSOCredW function [Security], security.creduistoressocredw, wincred/CredUIStoreSSOCredW
req.header: wincred.h
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
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredUIStoreSSOCredW
 - wincred/CredUIStoreSSOCredW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUIStoreSSOCredW
---

# CredUIStoreSSOCredW function


## -description

The <b>CredUIStoreSSOCredW</b> function stores a single logon credential.

## -parameters

### -param pszRealm [in]

Pointer to a <b>null</b>-terminated string that specifies the realm. If this parameter is <b>NULL</b>, the default realm is used.

### -param pszUsername [in]

Pointer to a <b>null</b>-terminated string that specifies the user's name.

### -param pszPassword [in]

Pointer to a <b>null</b>-terminated string that specifies the user's password. When you have finished using the password, clear the password from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param bPersist [in]

Boolean value that specifies whether the credentials are persisted. If this value is <b>TRUE</b>, the credentials are persisted. If this value is <b>FALSE</b>, the credentials are not persisted.

## -returns

The return value is a <b>DWORD</b>. A return value of ERROR_SUCCESS indicates the function was successful.

## -see-also

<a href="/windows/desktop/api/wincred/nf-wincred-creduireadssocredw">CredUIReadSSOCredW</a>