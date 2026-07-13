---
UID: NF:winldap.ldap_searchW
title: ldap_searchW function (winldap.h)
description: The ldap_searchW (Unicode) function (winldap.h) searches the LDAP directory and returns a requested set of attributes for each matched entry. 
helpviewer_keywords: ["LDAP_SCOPE_BASE", "LDAP_SCOPE_ONELEVEL", "LDAP_SCOPE_SUBTREE", "_ldap_ldap_search", "ldap.ldap__search", "ldap.ldap_search", "ldap_search", "ldap_search function [LDAP]", "ldap_searchW", "winldap/ldap_search", "winldap/ldap_searchW"]
old-location: ldap\ldap_search.htm
tech.root: ldap
ms.assetid: fe0d782b-8faf-4666-a952-e2bfd33f6d67
ms.date: 08/04/2022
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search, ldap.ldap__search, ldap.ldap_search, ldap_search, ldap_search function [LDAP], ldap_searchA, ldap_searchW, winldap/ldap_search, winldap/ldap_searchA, winldap/ldap_searchW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_searchW (Unicode) and ldap_searchA (ANSI)
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
 - ldap_searchW
 - winldap/ldap_searchW
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
 - ldap_search
 - ldap_searchA
 - ldap_searchW
---

# ldap_searchW function


## -description

The <b>ldap_search</b> function searches the LDAP directory and returns a requested set of attributes for each matched entry.

## -parameters

### -param ld [in]

A session handle.

### -param base [in]

A pointer to a null-terminated string that contains the distinguished name of the entry at which to start the search.

### -param scope [in]

A data type that specifies one of the following values to indicate the search scope.



#### LDAP_SCOPE_BASE

Search only the base entry.



#### LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.



#### LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.

### -param filter [in]

A pointer to a null-terminated string that specifies the search filter. For more information, see 
<a href="/windows/desktop/ADSI/search-filter-syntax">Search Filter Syntax</a>.

### -param attrs [in]

A null-terminated array of null-terminated strings that indicate which attributes to return for each matching entry. Pass <b>NULL</b> to retrieve available attributes.

### -param attrsonly [in]

Boolean value that should be zero if both attribute types and values are to be returned, nonzero if only types are required.


##### - scope.LDAP_SCOPE_BASE

Search only the base entry.


##### - scope.LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.


##### - scope.LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.

## -returns

If the function succeeds, it returns the message ID of the search operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.

## -remarks

The <b>ldap_search</b> function initiates an asynchronous search operation.

Use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> function with the <i>ld</i> session handle to set the LDAP_OPT_SIZELIMIT, LDAP_OPT_TIMELIMIT, and LDAP_OPT_DEREF options that determine how the search is performed. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>.

As an asynchronous function, <b>ldap_search</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous search operation before it has completed, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

To have the function return the results directly, use the synchronous routine 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a> to implement support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_search</b> are thread-safe, provided that 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldapgetlasterror">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>




> [!NOTE]
> The winldap.h header defines ldap_search as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind">ldap_bind</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_simple_bind">ldap_simple_bind</a>
