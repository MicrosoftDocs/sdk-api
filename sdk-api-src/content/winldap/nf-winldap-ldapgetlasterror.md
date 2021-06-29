---
UID: NF:winldap.LdapGetLastError
title: LdapGetLastError function (winldap.h)
description: The LdapGetLastError function retrieves the last error code returned by an LDAP call.
helpviewer_keywords: ["LdapGetLastError","LdapGetLastError function [LDAP]","_ldap_ldapgetlasterror","ldap.ldapgetlasterror","winldap/LdapGetLastError"]
old-location: ldap\ldapgetlasterror.htm
tech.root: ldap
ms.assetid: 04bcdd90-344a-4f2d-a700-e725584e49d9
ms.date: 12/05/2018
ms.keywords: LdapGetLastError, LdapGetLastError function [LDAP], _ldap_ldapgetlasterror, ldap.ldapgetlasterror, winldap/LdapGetLastError
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
 - LdapGetLastError
 - winldap/LdapGetLastError
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
 - LdapGetLastError
---

# LdapGetLastError function


## -description

The <b>LdapGetLastError</b> function retrieves the last error code returned by an LDAP call.



## -returns

An LDAP error code.

## -remarks

The <b>LdapGetLastError</b> function returns the LDAP error code for the last LDAP operation on the thread that is calling it. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for a list of possible error codes.

Multithreading: The <b>LdapGetLastError</b> function is thread-safe.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>
