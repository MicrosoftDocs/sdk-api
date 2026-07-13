---
UID: NF:winldap.ldap_modrdn2_sA
title: ldap_modrdn2_sA function (winldap.h)
description: The ldap_modrdn2_s function changes the relative distinguished name of an LDAP entry. (ldap_modrdn2_sA)
helpviewer_keywords: ["ldap.ldap__modrdn2__s", "ldap_modrdn2_sA", "winldap/ldap_modrdn2_sA"]
old-location: ldap\ldap_modrdn2_s.htm
tech.root: ldap
ms.assetid: a2cf121d-4e84-4195-9080-3b6c0c4cea82
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_modrdn2_s, ldap.ldap__modrdn2__s, ldap.ldap_modrdn2_s, ldap_modrdn2_s, ldap_modrdn2_s function [LDAP], ldap_modrdn2_sA, ldap_modrdn2_sW, winldap/ldap_modrdn2_s, winldap/ldap_modrdn2_sA, winldap/ldap_modrdn2_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdn2_sW (Unicode) and ldap_modrdn2_sA (ANSI)
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
 - ldap_modrdn2_sA
 - winldap/ldap_modrdn2_sA
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
 - ldap_modrdn2_s
 - ldap_modrdn2_sA
 - ldap_modrdn2_sW
---

# ldap_modrdn2_sA function


## -description

The <b>ldap_modrdn2_s</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete. For LDAP 3 or later, use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a> functions.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name to change.

### -param NewDistinguishedName [in]

A pointer to a null-terminated string that contains the new relative distinguished name to give the entry.

### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Be aware that the various <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn">ldap_modrdn</a> functions allow you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation that allows access to name-change functions. This feature is available by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>. These functions are recommended, rather than the <b>ldap_modrdn2_s</b> function, to change an entry name.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting any other operations.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2">ldap_modrdn2</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
