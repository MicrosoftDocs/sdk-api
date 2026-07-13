---
UID: NF:winldap.ldap_modrdn_sW
title: ldap_modrdn_sW function (winldap.h)
description: The ldap_modrdn_sW (Unicode) function (winldap.h) changes the relative distinguished name of an LDAP entry.  
helpviewer_keywords: ["_ldap_ldap_modrdn_s", "ldap.ldap__modrdn__s", "ldap.ldap_modrdn_s", "ldap_modrdn_s", "ldap_modrdn_s function [LDAP]", "ldap_modrdn_sW", "winldap/ldap_modrdn_s", "winldap/ldap_modrdn_sW"]
old-location: ldap\ldap_modrdn_s.htm
tech.root: ldap
ms.assetid: 0ea0c52d-5056-4ccf-bc64-87a2f0ebd0c5
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_modrdn_s, ldap.ldap__modrdn__s, ldap.ldap_modrdn_s, ldap_modrdn_s, ldap_modrdn_s function [LDAP], ldap_modrdn_sA, ldap_modrdn_sW, winldap/ldap_modrdn_s, winldap/ldap_modrdn_sA, winldap/ldap_modrdn_sW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdn_sW (Unicode) and ldap_modrdn_sA (ANSI)
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
 - ldap_modrdn_sW
 - winldap/ldap_modrdn_sW
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
 - ldap_modrdn_s
 - ldap_modrdn_sA
 - ldap_modrdn_sW
---

# ldap_modrdn_sW function


## -description

The <b>ldap_modrdn_s</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete and is provided for backward compatibility with earlier versions of LDAP. For LDAP 3 or later, use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a> function.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to be changed.

### -param NewDistinguishedName [out]

A pointer to a null-terminated string that contains the new relative distinguished name to give the entry.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Use the <b>ldap_modrdn_s</b> function, or its asynchronous equivalent, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn">ldap_modrdn</a>, to change the name of an LDAP entry. This function provides compatibility with LDAP 1. Otherwise, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2">ldap_modrdn2</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>.

Be aware that the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn">ldap_modrdn</a> functions enable you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation that allows more general name change access. This feature is available by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>. These functions are  recommended, instead of the <b>ldap_modrdn_s</b> function, to change an entry name.





> [!NOTE]
> The winldap.h header defines ldap_modrdn_s as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn">ldap_modrdn</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2">ldap_modrdn2</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modrdn2_s">ldap_modrdn2_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext">ldap_rename_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_rename_ext_s">ldap_rename_ext_s</a>
