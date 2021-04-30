---
UID: NF:winldap.ldap_count_entries
title: ldap_count_entries function (winldap.h)
description: The ldap_count_entries function counts the number of search entries that a server returned.
helpviewer_keywords: ["_ldap_ldap_count_entries","ldap.ldap__count__entries","ldap.ldap_count_entries","ldap_count_entries","ldap_count_entries function [LDAP]","winldap/ldap_count_entries"]
old-location: ldap\ldap_count_entries.htm
tech.root: ldap
ms.assetid: 6e53b914-2ad8-408a-9671-50a01a8a42f1
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_count_entries, ldap.ldap__count__entries, ldap.ldap_count_entries, ldap_count_entries, ldap_count_entries function [LDAP], winldap/ldap_count_entries
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
 - ldap_count_entries
 - winldap/ldap_count_entries
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
 - ldap_count_entries
---

# ldap_count_entries function


## -description

The <b>ldap_count_entries</b> function counts the number of search entries that a server returned.

## -parameters

### -param ld [in]

The session handle.

### -param res [in]

The search result obtained by a call to one of the synchronous search routines or to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -returns

If the function succeeds, it returns the number of entries.

If the function fails, the return value is –1 and the function sets the session error parameters in the LDAP data structure.

## -remarks

The <b>ldap_count_entries</b> function returns the number of entries contained, or remaining in a chain of entries. Call the function with the return value from 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_reference">ldap_first_reference</a>, 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a>, or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_references">ldap_count_references</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_entry">ldap_first_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_first_reference">ldap_first_reference</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_entry">ldap_next_entry</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_next_reference">ldap_next_reference</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>