---
UID: NF:winldap.ldap_modify_s
title: ldap_modify_s function (winldap.h)
description: The ldap_modify_s function (winldap.h) initiates an asynchronous operation to modify an existing entry.
helpviewer_keywords: ["_ldap_ldap_modify_s","ldap.ldap__modify__s","ldap.ldap_modify_s","ldap_modify_s","ldap_modify_s function [LDAP]","ldap_modify_sA","ldap_modify_sW","winldap/ldap_modify_s","winldap/ldap_modify_sA","winldap/ldap_modify_sW"]
old-location: ldap\ldap_modify_s.htm
tech.root: ldap
ms.assetid: 26002d58-a4ac-4fd6-aa63-39210f8fc883
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modify_s, ldap.ldap__modify__s, ldap.ldap_modify_s, ldap_modify_s, ldap_modify_s function [LDAP], ldap_modify_sA, ldap_modify_sW, winldap/ldap_modify_s, winldap/ldap_modify_sA, winldap/ldap_modify_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modify_sW (Unicode) and ldap_modify_sA (ANSI)
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
 - ldap_modify_s
 - winldap/ldap_modify_s
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
 - ldap_modify_s
 - ldap_modify_sA
 - ldap_modify_sW
---

# ldap_modify_s function


## -description

The <b>ldap_modify_s</b> function changes an existing entry.

## -parameters

### -param ld [in]

The session handle.

### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.

### -param mods [in]

A null-terminated array of modifications to make to the entry.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

The <b>ldap_modify_s</b> function initiates a synchronous operation to modify an existing entry. If values are being added to or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, the function removes the attribute if no values remain. All modifications are performed in the order in which they are listed.

Multithreading: Calls to <b>ldap_modify_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapmoda">LDAPMod</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext">ldap_modify_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s">ldap_modify_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
