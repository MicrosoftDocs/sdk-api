---
UID: NF:winldap.ldap_count_references
title: ldap_count_references function (winldap.h)
description: The ldap_count_references function counts the number of subordinate references that were returned by the server in a response to a search request.
helpviewer_keywords: ["_ldap_ldap_count_references","ldap.ldap__count__references","ldap.ldap_count_references","ldap_count_references","ldap_count_references function [LDAP]","winldap/ldap_count_references"]
old-location: ldap\ldap_count_references.htm
tech.root: ldap
ms.assetid: 1d216f39-6eb4-4c3d-8f97-92835aac2aca
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_count_references, ldap.ldap__count__references, ldap.ldap_count_references, ldap_count_references, ldap_count_references function [LDAP], winldap/ldap_count_references
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
 - ldap_count_references
 - winldap/ldap_count_references
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
 - ldap_count_references
---

# ldap_count_references function


## -description

The <b>ldap_count_references</b> function counts the number of subordinate references that were returned by the server in a response to a search request.

## -parameters

### -param ld [in]

The session handle.

### -param res [in]

The search result obtained by a call to one of the synchronous search routines or to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -returns

If the function succeeds, it returns the number of references.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.

## -remarks

The <b>ldap_count_references</b> function returns the number of references contained in a chain of search results. It can also be used to count the number of references that remain in a chain. Call the function with the return value from 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_reference">ldap_first_reference</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a>, or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_entries">ldap_count_entries</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_reference">ldap_first_reference</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>