---
UID: NF:winldap.ldap_search_init_pageW
title: ldap_search_init_pageW function
author: windows-driver-content
description: Initializes a search block for a simple paged-results search.
old-location: ldap\ldap_search_init_page.htm
old-project: LDAP
ms.assetid: f88d32e3-ac5f-4934-bf84-4007ffd72ac2
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search_init_page, ldap.ldap__search__init__page, ldap.ldap_search_init_page, ldap_search_init_page, ldap_search_init_page function [LDAP], ldap_search_init_pageA, ldap_search_init_pageW, winldap/ldap_search_init_page, winldap/ldap_search_init_pageA, winldap/ldap_search_init_pageW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_search_init_pageW (Unicode) and ldap_search_init_pageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_search_init_page
-	ldap_search_init_pageA
-	ldap_search_init_pageW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_search_init_pageW function


## -description


The <b>ldap_search_init_page</b> function initializes a search block for a simple paged-results search. This function is supported in LDAP 3.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name of the entry at which to start the search.


### -param ScopeOfSearch [in]

A data type that specifies one of the following values to indicate the scope of the search.



#### LDAP_SCOPE_BASE

Search the base entry only.



#### LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.



#### LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.


### -param SearchFilter [in]

A pointer to a null-terminated string that specifies the search filter. For more information, see 
<a href="https://msdn.microsoft.com/3ce4709c-5ef7-4713-8fb7-b46ab284339f">Search Filter Syntax</a>.


### -param AttributeList [in]

A null-terminated array of null-terminated strings indicating which attributes to return for each matching entry. Pass <b>NULL</b> to retrieve all available attributes.


### -param AttributesOnly [in]

A Boolean value that should be zero if both attribute types and values are to be returned, nonzero if only types are to be returned.


### -param ServerControls [in]

A list of LDAP server controls.


### -param ClientControls [in]

A list of client controls.


### -param PageTimeLimit [in]

The time value, in seconds, that the client will wait for the server to return a page.


### -param TotalSizeLimit [in]

The maximum number of entries the client will accept.  The <i>TotalSizeLimit</i> value affects only the individual pages within the paged search (not the overall paged search).  So if <i>TotalSizeLimit</i> is greater than page size, then <i>TotalSizeLimit</i> will have no effect.


### -param SortKeys [in]

A pointer to an 
<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a> structure, which specifies the attribute type, the ordering rule, and the direction for the search.


##### - ScopeOfSearch.LDAP_SCOPE_BASE

Search the base entry only.


##### - ScopeOfSearch.LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.


##### - ScopeOfSearch.LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.


## -returns



If the function succeeds, it returns a pointer to an 
<a href="https://msdn.microsoft.com/70bdbb05-ac7f-48af-9241-e2a70b6b16ab">LDAPSearch</a> structure.

If the function fails, the return value is <b>NULL</b>. Use 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> or 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error code.

Call the <a href="https://msdn.microsoft.com/0c434611-b4d0-46e4-8e81-fc221e63de9f">ldap_search_abandon_page</a> to free the returned structure.




## -remarks



The 
<b>ldap_search_init_page</b> function creates an LDAPSearch structure for managing paged searches and returns a handle to the structure. The 
<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>, 
<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>, and 
<a href="https://msdn.microsoft.com/17ad1c7e-c3a1-4f6a-8303-fbbedfc36409">ldap_get_paged_count</a> functions require this search handle as a parameter. When the paged search is completed, call 
<a href="https://msdn.microsoft.com/0c434611-b4d0-46e4-8e81-fc221e63de9f">ldap_search_abandon_page</a> to free this structure and its handle.

To determine whether a server supports paged-results searches, check the supportedControl property off of the root for an object identifier (OID) of 1.2.840.113556.1.4.319.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/70bdbb05-ac7f-48af-9241-e2a70b6b16ab">LDAPSearch</a>



<a href="https://msdn.microsoft.com/3cf6a279-5ea4-48f3-bdc7-768f64b1bf7c">LDAPSortKey</a>



<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a>



<a href="https://msdn.microsoft.com/34ddf4d4-3a89-42e0-850d-fcc1c942cb3b">ldap_get_next_page</a>



<a href="https://msdn.microsoft.com/44b1b298-9796-4627-945e-4051c20f3c92">ldap_get_next_page_s</a>



<a href="https://msdn.microsoft.com/0c434611-b4d0-46e4-8e81-fc221e63de9f">ldap_search_abandon_page</a>
 

 

