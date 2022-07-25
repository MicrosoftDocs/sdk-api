---
UID: NS:wtypesbase._COAUTHIDENTITY
title: COAUTHIDENTITY (wtypesbase.h)
description: Contains a user name and password.
helpviewer_keywords: ["COAUTHIDENTITY","COAUTHIDENTITY structure [COM]","SEC_WINNT_AUTH_IDENTITY_ANSI","SEC_WINNT_AUTH_IDENTITY_UNICODE","_COAUTHIDENTITY","_com_COAUTHIDENTITY","com.coauthidentity","wtypesbase/COAUTHIDENTITY"]
old-location: com\coauthidentity.htm
tech.root: com
ms.assetid: ce14f8a6-0495-491a-a5c7-de7c1d3efd95
ms.date: 12/05/2018
ms.keywords: COAUTHIDENTITY, COAUTHIDENTITY structure [COM], SEC_WINNT_AUTH_IDENTITY_ANSI, SEC_WINNT_AUTH_IDENTITY_UNICODE, _COAUTHIDENTITY, _com_COAUTHIDENTITY, com.coauthidentity, wtypesbase/COAUTHIDENTITY
req.header: wtypesbase.h
req.include-header: WTypes.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COAUTHIDENTITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COAUTHIDENTITY
 - wtypesbase/_COAUTHIDENTITY
 - COAUTHIDENTITY
 - wtypesbase/COAUTHIDENTITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - COAUTHIDENTITY
---

# COAUTHIDENTITY structure


## -description

Contains a user name and password.

## -struct-fields

### -field User

The user's name.

### -field UserLength

The length of the <b>User</b> string, without the terminating <b>NULL</b>.

### -field Domain

The domain or workgroup name.

### -field DomainLength

The length of the <b>Domain</b> string, without the terminating <b>NULL</b>.

### -field Password

The user's password in the domain or workgroup.

### -field PasswordLength

The length of the <b>Password</b> string, without the terminating <b>NULL</b>.

### -field Flags

Indicates whether the strings are Unicode strings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_ANSI"></a><a id="sec_winnt_auth_identity_ansi"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_ANSI</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The strings are ANSI strings.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WINNT_AUTH_IDENTITY_UNICODE"></a><a id="sec_winnt_auth_identity_unicode"></a><dl>
<dt><b>SEC_WINNT_AUTH_IDENTITY_UNICODE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The strings are Unicode strings.

</td>
</tr>
</table>

## -remarks

COM does not persist the user's password information. For applications that use passwords, please see the documentation on <a href="/windows/desktop/SecCrypto/cryptography-portal">Cryptography</a> (CryptoAPI). 


This structure is equivalent to the <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> structure.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo">COAUTHINFO</a>