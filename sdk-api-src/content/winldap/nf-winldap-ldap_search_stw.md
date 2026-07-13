---
UID: NF:winldap.ldap_search_stW
title: ldap_search_stW function (winldap.h)
description: The ldap_search_stW (Unicode) function (winldap.h) synchronously searches the LDAP directory and returns a requested set of attributes for each entry matched.  
helpviewer_keywords: ["LDAP_SCOPE_BASE", "LDAP_SCOPE_ONELEVEL", "LDAP_SCOPE_SUBTREE", "_ldap_ldap_search_st", "ldap.ldap__search__st", "ldap.ldap_search_st", "ldap_search_st", "ldap_search_st function [LDAP]", "ldap_search_stW", "winldap/ldap_search_st", "winldap/ldap_search_stW"]
old-location: ldap\ldap_search_st.htm
tech.root: ldap
ms.assetid: af2ab469-fa72-4a57-912c-42d9a6721806
ms.date: 08/04/2022
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search_st, ldap.ldap__search__st, ldap.ldap_search_st, ldap_search_st, ldap_search_st function [LDAP], ldap_search_stA, ldap_search_stW, winldap/ldap_search_st, winldap/ldap_search_stA, winldap/ldap_search_stW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_search_stW (Unicode) and ldap_search_stA (ANSI)
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
 - ldap_search_stW
 - winldap/ldap_search_stW
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
 - ldap_search_st
 - ldap_search_stA
 - ldap_search_stW
---

# ldap_search_stW function


## -description

The <b>ldap_search_st</b> function synchronously searches the LDAP directory and returns a requested set of attributes for each entry matched. An additional parameter  specifies a local time-out for the search. The function is identical to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>, except for the additional local time-out parameter.

## -parameters

### -param ld [in]

Session handle.

### -param base [in]

Pointer to a null-terminated string that contains the distinguished name of the entry at which to start the search.

### -param scope [in]

Specifies one of the following values to indicate the search scope.



#### LDAP_SCOPE_BASE

Search the base entry only.



#### LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.



#### LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.

### -param filter [in]

Pointer to a null-terminated string that specifies the search filter. For more information, see 
<a href="/windows/desktop/ADSI/search-filter-syntax">Search Filter Syntax</a>.

### -param attrs [in]

A null-terminated array of null-terminated strings that indicate which attributes to return for each matching entry. Pass <b>NULL</b> to retrieve all available attributes.

### -param attrsonly [in]

Boolean value that must be zero if both attribute types and values are to be returned, nonzero if only types are required.

### -param timeout [in]

The local search time-out value, in seconds.

### -param res [out]

Contains the results of the search upon completion of the call. Can also contain partial results or extended data when the function call fails with an error code. Any results returned must be freed with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a> when  no longer required by the application.


##### - scope.LDAP_SCOPE_BASE

Search the base entry only.


##### - scope.LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.


##### - scope.LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code, however <b>ldap_search_st</b> can fail and can still allocate <i>pMsg</i>. For example, both <b>LDAP_PARTIAL_RESULTS</b> and <b>LDAP_REFERRAL</b> error code allocate <i>pMsg</i>. For more information, see the following code example. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_search_st</b> function initiates a synchronous search operation.

Use the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a> function with the <i>ld</i> session handle to set the <b>LDAP_OPT_SIZELIMIT</b> and <b>LDAP_OPT_DEREF</b> options that determine how the search is performed. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>. The <i>timeout</i> parameter in <b>ldap_search_st</b> overrides the <b>LDAP_OPT_TIMELIMIT</b>.

Upon completion of the search operation, <b>ldap_search_st</b> returns to the caller. Use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search">ldap_search</a> or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a> to have the operation performed asynchronously.

Multithreading: Calls to <b>ldap_search_st</b> are thread-safe.

The following code example shows how to free <i>pMsg</i> if <b>ldap_search_st</b> fails.


```cpp
// Initialize return value to NULL.
LDAPMessage *pMsg = NULL;

// Perform the search request.
dwErr = ldap_search_st (i_pldap,
        i_lpszBase,
        i_ulScope,
        i_lpszSearchFilter,
        lpszAttributes,
        0,
        lpsTimeout,
        &pMsg
        );

// Cleanup calling parameters.
if (lpszAttributes != NULL)
    delete [] lpszAttributes;

// Convert error code and cleanup pMsg if necessary.
if (dwErr != LDAP_SUCCESS)
{
    DebugOutLDAPError(i_pldap, dwErr, _T("ldap_search_st"));
    hr = HRESULT_FROM_WIN32(dwErr);

    // Be aware that pMsg can contain valid data, even if the
    // call to ldap_search_st returned an error code.  
    // This can be caused by the server returning codes,
    // such as LDAP_RESULTS_TOO_LARGE or other codes,
    // that indicate that the search returned partial
    // results. The user code can handle these cases
    // if required, this example just frees pMsg on any 
    // error code.

    if (pMsg != NULL)
      ldap_msgfree(pMsg);
}

else
{
    // Process the search results.
    ...
    // Free the results when complete.
    if (pMsg != NULL) ldap_msgfree(pMsg);
}
```






> [!NOTE]
> The winldap.h header defines ldap_search_st as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search">ldap_search</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>
