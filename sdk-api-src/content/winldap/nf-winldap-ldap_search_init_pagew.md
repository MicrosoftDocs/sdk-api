---
UID: NF:winldap.ldap_search_init_pageW
title: ldap_search_init_pageW function (winldap.h)
description: The ldap_search_init_pageW (Unicode) function (winldap.h) initializes a search block for a simple paged-results search.
helpviewer_keywords: ["LDAP_SCOPE_BASE", "LDAP_SCOPE_ONELEVEL", "LDAP_SCOPE_SUBTREE", "_ldap_ldap_search_init_page", "ldap.ldap__search__init__page", "ldap.ldap_search_init_page", "ldap_search_init_page", "ldap_search_init_page function [LDAP]", "ldap_search_init_pageW", "winldap/ldap_search_init_page", "winldap/ldap_search_init_pageW"]
old-location: ldap\ldap_search_init_page.htm
tech.root: ldap
ms.assetid: f88d32e3-ac5f-4934-bf84-4007ffd72ac2
ms.date: 08/04/2022
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search_init_page, ldap.ldap__search__init__page, ldap.ldap_search_init_page, ldap_search_init_page, ldap_search_init_page function [LDAP], ldap_search_init_pageA, ldap_search_init_pageW, winldap/ldap_search_init_page, winldap/ldap_search_init_pageA, winldap/ldap_search_init_pageW
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
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_search_init_pageW
 - winldap/ldap_search_init_pageW
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
 - ldap_search_init_page
 - ldap_search_init_pageA
 - ldap_search_init_pageW
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
<a href="/windows/desktop/ADSI/search-filter-syntax">Search Filter Syntax</a>.

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
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a> structure, which specifies the attribute type, the ordering rule, and the direction for the search.


##### - ScopeOfSearch.LDAP_SCOPE_BASE

Search the base entry only.


##### - ScopeOfSearch.LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.


##### - ScopeOfSearch.LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.

## -returns

If the function succeeds, it returns a pointer to an 
<a href="/previous-versions/windows/desktop/legacy/aa366129(v=vs.85)">LDAPSearch</a> structure.

If the function fails, the return value is <b>NULL</b>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> or 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to retrieve the error code.

Call the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_abandon_page">ldap_search_abandon_page</a> to free the returned structure.

## -remarks

The 
<b>ldap_search_init_page</b> function creates an LDAPSearch structure for managing paged searches and returns a handle to the structure. The 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>, and 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_paged_count">ldap_get_paged_count</a> functions require this search handle as a parameter. When the paged search is completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_abandon_page">ldap_search_abandon_page</a> to free this structure and its handle.

To determine whether a server supports paged-results searches, check the supportedControl property off of the root for an object identifier (OID) of 1.2.840.113556.1.4.319.





> [!NOTE]
> The winldap.h header defines ldap_search_init_page as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/previous-versions/windows/desktop/legacy/aa366129(v=vs.85)">LDAPSearch</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page">ldap_get_next_page</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_next_page_s">ldap_get_next_page_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_abandon_page">ldap_search_abandon_page</a>
