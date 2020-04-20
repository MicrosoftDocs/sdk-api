---
UID: NS:winldap.ldapsortkeyA
title: LDAPSortKeyA (winldap.h)
description: The LDAPSortKey structure stores sorting criteria for use by sort controls.helpviewer_keywords: ["*PLDAPSortKeyA","LDAPSortKey","LDAPSortKey structure [LDAP]","LDAPSortKeyA","LDAPSortKeyW","PLDAPSortKey","PLDAPSortKey structure pointer [LDAP]","_ldap_ldapsortkey","ldap.ldapsortkey","winldap/LDAPSortKey","winldap/LDAPSortKeyA","winldap/LDAPSortKeyW","winldap/PLDAPSortKey"]
old-location: ldap\ldapsortkey.htm
tech.root: ldap
ms.assetid: 3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c
ms.date: 12/05/2018
ms.keywords: '*PLDAPSortKeyA, LDAPSortKey, LDAPSortKey structure [LDAP], LDAPSortKeyA, LDAPSortKeyW, PLDAPSortKey, PLDAPSortKey structure pointer [LDAP], _ldap_ldapsortkey, ldap.ldapsortkey, winldap/LDAPSortKey, winldap/LDAPSortKeyA, winldap/LDAPSortKeyW, winldap/PLDAPSortKey'
f1_keywords:
- winldap/LDAPSortKey
dev_langs:
- c++
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
targetos: Windows
req.typenames: LDAPSortKeyA, *PLDAPSortKeyA
req.redist: 
ms.custom: 19H1
---

# LDAPSortKeyA structure


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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a> and 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a> functions use this structure to specify how results should be sorted before being returned to the client.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-server-sort-oid">LDAP_SERVER_SORT_OID</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_init_page">ldap_search_init_page</a>
 

 

