---
UID: NS:winldap.ldapsortkeyW
title: LDAPSortKeyW (winldap.h)
description: The LDAPSortKey structure stores sorting criteria for use by sort controls. (Unicode)
helpviewer_keywords: ["*PLDAPSortKeyW","LDAPSortKey","LDAPSortKey structure [LDAP]","LDAPSortKeyA","LDAPSortKeyW","PLDAPSortKey","PLDAPSortKey structure pointer [LDAP]","_ldap_ldapsortkey","ldap.ldapsortkey","winldap/LDAPSortKey","winldap/LDAPSortKeyA","winldap/LDAPSortKeyW","winldap/PLDAPSortKey"]
old-location: ldap\ldapsortkey.htm
tech.root: ldap
ms.assetid: 3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c
ms.date: 12/05/2018
ms.keywords: '*PLDAPSortKeyW, LDAPSortKey, LDAPSortKey structure [LDAP], LDAPSortKeyA, LDAPSortKeyW, PLDAPSortKey, PLDAPSortKey structure pointer [LDAP], _ldap_ldapsortkey, ldap.ldapsortkey, winldap/LDAPSortKey, winldap/LDAPSortKeyA, winldap/LDAPSortKeyW, winldap/PLDAPSortKey'
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LDAPSortKeyW (Unicode) and LDAPSortKeyA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPSortKeyW, *PLDAPSortKeyW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldapsortkeyW
 - winldap/ldapsortkeyW
 - PLDAPSortKeyW
 - winldap/PLDAPSortKeyW
 - LDAPSortKeyW
 - winldap/LDAPSortKeyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPSortKey
 - LDAPSortKeyA
 - LDAPSortKeyW
---

# LDAPSortKeyW structure


## -description

The <b>LDAPSortKey</b> structure stores sorting criteria for use by sort controls.

## -struct-fields

### -field sk_attrtype

Pointer to a null-terminated string that specifies the name of the attribute to use as a sort key. Use multiple <b>LDAPSortKey</b> structures to specify multiple sort keys. Be aware that Active Directory supports only a single sort key.

### -field sk_matchruleoid

Pointer to a null-terminated string that specifies the object identifier of the matching rule for the sort. Should be set to <b>NULL</b> if you do not want to explicitly specify a matching rule for the sort. Specifying an explicitly set matching rule is supported only by Windows Server 2003.

### -field sk_reverseorder

If <b>TRUE</b>, specifies that the sort be ordered from lowest to highest. If <b>FALSE</b>, the sort order is from highest to lowest.

## -remarks

The 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a> and 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a> functions use this structure to specify how results should be sorted before being returned to the client.





> [!NOTE]
> The winldap.h header defines LDAPSortKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/ldap/ldap-server-sort-oid">LDAP_SERVER_SORT_OID</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a>
