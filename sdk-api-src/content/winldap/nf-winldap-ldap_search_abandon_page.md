---
UID: NF:winldap.ldap_search_abandon_page
title: ldap_search_abandon_page function (winldap.h)
description: The ldap_search_abandon_page function terminates a paged-results search.
helpviewer_keywords: ["_ldap_ldap_search_abandon_page","ldap.ldap__search__abandon__page","ldap.ldap_search_abandon_page","ldap_search_abandon_page","ldap_search_abandon_page function [LDAP]","winldap/ldap_search_abandon_page"]
old-location: ldap\ldap_search_abandon_page.htm
tech.root: ldap
ms.assetid: 0c434611-b4d0-46e4-8e81-fc221e63de9f
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_search_abandon_page, ldap.ldap__search__abandon__page, ldap.ldap_search_abandon_page, ldap_search_abandon_page, ldap_search_abandon_page function [LDAP], winldap/ldap_search_abandon_page
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ldap_search_abandon_page
 - winldap/ldap_search_abandon_page
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
 - ldap_search_abandon_page
---

# ldap_search_abandon_page function


## -description

The <b>ldap_search_abandon_page</b> function terminates a paged-results search.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param SearchBlock [in]

A handle to the search block for the current search.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.

## -remarks

Call <b>ldap_search_abandon_page</b> after a search has completed (when the server returns <b>LDAP_NO_RESULTS_RETURNED</b>) to perform necessary cleanup. You can also use this function to abandon a search at any time after the search block has been allocated.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>