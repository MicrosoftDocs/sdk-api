---
UID: NF:winldap.ldap_explode_dnA
title: ldap_explode_dnA function (winldap.h)
description: The ldap_explode_dn function breaks up an entry name into its component parts. (ldap_explode_dnA)
helpviewer_keywords: ["ldap.ldap__explode__dn", "ldap_explode_dnA", "winldap/ldap_explode_dnA"]
old-location: ldap\ldap_explode_dn.htm
tech.root: ldap
ms.assetid: 9d151adf-f8b2-4ed1-8e25-86c95a89a948
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_explode_dn, ldap.ldap__explode__dn, ldap.ldap_explode_dn, ldap_explode_dn, ldap_explode_dn function [LDAP], ldap_explode_dnA, ldap_explode_dnW, winldap/ldap_explode_dn, winldap/ldap_explode_dnA, winldap/ldap_explode_dnW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_explode_dnW (Unicode) and ldap_explode_dnA (ANSI)
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
 - ldap_explode_dnA
 - winldap/ldap_explode_dnA
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
 - ldap_explode_dn
 - ldap_explode_dnA
 - ldap_explode_dnW
---

# ldap_explode_dnA function


## -description

The <b>ldap_explode_dn</b> function breaks up an entry name into its component parts.

## -parameters

### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name to explode.  The string that this pointer refers to cannot be a constant string.

### -param notypes [in]

Indicates whether the type information components should be removed.

## -returns

If the function succeeds, it returns a null-terminated character array containing the relative distinguished name components of the distinguished name supplied.

## -remarks

Call <b>ldap_explode_dn</b> to separate a distinguished name into its component parts. Set the <i>notypes</i> parameter to a nonzero value to remove type information, such as "cn=" from the components. The components of the relative distinguished name are returned in a character array. Free this array when it is no longer needed by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>.

Calling <b>ldap_explode_dn</b> with a pointer to a constant string will cause the function to fail.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>
