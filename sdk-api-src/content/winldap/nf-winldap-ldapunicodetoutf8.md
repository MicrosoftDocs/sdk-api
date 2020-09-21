---
UID: NF:winldap.LdapUnicodeToUTF8
title: LdapUnicodeToUTF8 function (winldap.h)
description: Converts Unicode strings to UTF-8.
helpviewer_keywords: ["LdapUnicodeToUTF8","LdapUnicodeToUTF8 function [LDAP]","_ldap_ldapunicodetoutf8","ldap.ldapunicodetoutf8","winldap/LdapUnicodeToUTF8"]
old-location: ldap\ldapunicodetoutf8.htm
tech.root: ldap
ms.assetid: 9a56cf0e-ff6c-4b0a-9138-495d9cebfc99
ms.date: 12/05/2018
ms.keywords: LdapUnicodeToUTF8, LdapUnicodeToUTF8 function [LDAP], _ldap_ldapunicodetoutf8, ldap.ldapunicodetoutf8, winldap/LdapUnicodeToUTF8
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LdapUnicodeToUTF8
 - winldap/LdapUnicodeToUTF8
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - LdapUnicodeToUTF8
---

# LdapUnicodeToUTF8 function


## -description

The <b>LdapUnicodeToUTF8</b> function converts Unicode strings to UTF-8. Modules that do not have the UTF-8 code page can call this function.

## -parameters

### -param lpSrcStr [in]

A pointer to a null-terminated Unicode string to convert.

### -param cchSrc [in]

An integer that specifies the size, in characters, of the <i>lpSrcStr</i> string.

### -param lpDestStr [out]

A pointer to a buffer that receives the converted UTF-8 character string, without a null terminator.

### -param cchDest [in]

An integer that specifies the size, in characters, of the <i>lpDestStr</i> buffer.

## -returns

The return value is the size, in characters, written to the <i>lpDestStr</i> buffer.
      If the <i>lpDestStr</i> buffer is too small, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

When the <i>cchDest</i> parameter is zero, the required size of the destination buffer is returned.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldaputf8tounicode">LdapUTF8ToUnicode</a>