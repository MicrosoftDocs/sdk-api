---
UID: NF:winldap.LdapUTF8ToUnicode
title: LdapUTF8ToUnicode function (winldap.h)
description: Used to translate strings for modules that do not have the UTF-8 code page.
helpviewer_keywords: ["LdapUTF8ToUnicode","LdapUTF8ToUnicode function [LDAP]","_ldap_ldaputf8tounicode","ldap.ldaputf8tounicode","winldap/LdapUTF8ToUnicode"]
old-location: ldap\ldaputf8tounicode.htm
tech.root: ldap
ms.assetid: 4c36ce90-8cc6-4dee-b990-5d283613ba11
ms.date: 12/05/2018
ms.keywords: LdapUTF8ToUnicode, LdapUTF8ToUnicode function [LDAP], _ldap_ldaputf8tounicode, ldap.ldaputf8tounicode, winldap/LdapUTF8ToUnicode
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
 - LdapUTF8ToUnicode
 - winldap/LdapUTF8ToUnicode
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
 - LdapUTF8ToUnicode
---

# LdapUTF8ToUnicode function


## -description

The <b>LdapUTF8ToUnicode</b> function is used to translate strings for modules that do not have the UTF-8 code page.

## -parameters

### -param lpSrcStr [in]

A pointer to a null-terminated UTF-8 string to convert.

### -param cchSrc [in]

An integer that specifies the size, in characters, of the <i>lpSrcStr</i> string.

### -param lpDestStr [out]

A pointer to a buffer that receives the converted Unicode string, without a null terminator.

### -param cchDest [in]

An integer that specifies the size, in characters, of the <i>lpDestStr</i> buffer.

## -returns

The return value is the number of characters written to the <i>lpDestStr</i> buffer.
      If the <i>lpDestStr</i> buffer is too small, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

When the <i>cchDest</i> parameter is zero, the required size of the destination buffer is returned.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapunicodetoutf8">LdapUnicodeToUTF8</a>