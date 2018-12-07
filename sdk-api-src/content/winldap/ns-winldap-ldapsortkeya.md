---
UID: NS:winldap.ldapsortkeyA
title: LDAPSortKeyA
author: windows-sdk-content
description: The LDAPSortKey structure stores sorting criteria for use by sort controls.
old-location: ldap\ldapsortkey.htm
tech.root: ldap
ms.assetid: 3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLDAPSortKeyA, LDAPSortKey, LDAPSortKey structure [LDAP], LDAPSortKeyA, LDAPSortKeyW, PLDAPSortKey, PLDAPSortKey structure pointer [LDAP], _ldap_ldapsortkey, ldap.ldapsortkey, winldap/LDAPSortKey, winldap/LDAPSortKeyA, winldap/LDAPSortKeyW, winldap/PLDAPSortKey"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: LDAPSortKeyA, *PLDAPSortKeyA
req.redist: 
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
<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a> and 
<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a> functions use this structure to specify how results should be sorted before being returned to the client.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/03c51778-45ed-46de-94a2-425bf7030cf0">LDAP_SERVER_SORT_OID</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/bbf8f860-ead8-4b22-8efa-0697076267ad">ldap_create_sort_control</a>



<a href="https://msdn.microsoft.com/f88d32e3-ac5f-4934-bf84-4007ffd72ac2">ldap_search_init_page</a>
 

 

