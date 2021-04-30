---
UID: NF:authz.AuthzAddSidsToContext
title: AuthzAddSidsToContext function (authz.h)
description: Creates a copy of an existing context and appends a given set of security identifiers (SIDs) and restricted SIDs.
helpviewer_keywords: ["AuthzAddSidsToContext","AuthzAddSidsToContext function [Security]","_win32_authzaddsidstocontext","authz/AuthzAddSidsToContext","security.authzaddsidstocontext"]
old-location: security\authzaddsidstocontext.htm
tech.root: security
ms.assetid: 4744013b-7f2e-4ebb-8944-10ffcc6006d0
ms.date: 12/05/2018
ms.keywords: AuthzAddSidsToContext, AuthzAddSidsToContext function [Security], _win32_authzaddsidstocontext, authz/AuthzAddSidsToContext, security.authzaddsidstocontext
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - AuthzAddSidsToContext
 - authz/AuthzAddSidsToContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzAddSidsToContext
---

# AuthzAddSidsToContext function


## -description

The <b>AuthzAddSidsToContext</b> function creates a copy of an existing context and appends a given set of <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) and restricted SIDs.

## -parameters

### -param hAuthzClientContext [in]

An <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure to be copied as the basis for <i>NewClientContext</i>.

### -param Sids [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structure containing the SIDs and attributes to be added to the unrestricted part of the client context.

### -param SidCount [in]

The number of SIDs to be added.

### -param RestrictedSids [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structure containing the SIDs and attributes to be added to the restricted part of the client context.

### -param RestrictedSidCount [in]

Number of restricted SIDs to be added.

### -param phNewAuthzClientContext [out]

A pointer to the created <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure containing input values for expiration time, identifier, flags, additional SIDs and restricted SIDs.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a>