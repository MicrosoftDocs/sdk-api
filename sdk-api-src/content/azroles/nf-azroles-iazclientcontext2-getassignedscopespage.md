---
UID: NF:azroles.IAzClientContext2.GetAssignedScopesPage
title: IAzClientContext2::GetAssignedScopesPage (azroles.h)
description: Retrieves a list of the scopes in which the client represented by the current IAzClientContext2 object is assigned to at least one role.
helpviewer_keywords: ["AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY","GetAssignedScopesPage","GetAssignedScopesPage method [Security]","GetAssignedScopesPage method [Security]","IAzClientContext2 interface","IAzClientContext2 interface [Security]","GetAssignedScopesPage method","IAzClientContext2.GetAssignedScopesPage","IAzClientContext2::GetAssignedScopesPage","azroles/IAzClientContext2::GetAssignedScopesPage","security.iazclientcontext2_getassignedscopespage"]
old-location: security\iazclientcontext2_getassignedscopespage.htm
tech.root: security
ms.assetid: 496dd834-37d9-41f6-a552-39c558dd60b3
ms.date: 12/05/2018
ms.keywords: AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY, GetAssignedScopesPage, GetAssignedScopesPage method [Security], GetAssignedScopesPage method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],GetAssignedScopesPage method, IAzClientContext2.GetAssignedScopesPage, IAzClientContext2::GetAssignedScopesPage, azroles/IAzClientContext2::GetAssignedScopesPage, security.iazclientcontext2_getassignedscopespage
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzClientContext2::GetAssignedScopesPage
 - azroles/IAzClientContext2::GetAssignedScopesPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext2.GetAssignedScopesPage
---

# IAzClientContext2::GetAssignedScopesPage


## -description

The <b>GetAssignedScopesPage</b> method retrieves a list of the scopes in which the client represented by the current <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> object is assigned to at least one role.

## -parameters

### -param lOptions [in]

A flag that specifies whether this method checks LDAP query groups for scope assignment. Previously cached LDAP query groups are checked regardless of the value of this flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY"></a><a id="az_client_context_skip_ldap_query"></a><dl>
<dt><b>AZ_CLIENT_CONTEXT_SKIP_LDAP_QUERY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
LDAP query groups that were not previously cached are not checked.

</td>
</tr>
</table>

### -param PageSize [in]

The number of elements in each page result.

### -param pvarCursor [in, out]

A pointer to a <b>VARIANT</b> that represents the current page of results. For the first call to the  <b>GetAssignedScopesPage</b> method, pass <b>VT_EMPTY</b> as the value for this parameter to retrieve the first page of results. The number of elements on a page is determined by the value of the <i>PageSize</i> parameter. On output, this parameter contains the value to be passed in the next call to <b>GetAssignedScopesPage</b> to retrieve the next page of results. If the value of this parameter on output is <b>EMPTY</b>, there are no more result pages.

### -param pvarScopeNames

On return, contains an array of variables of type <b>VARIANT</b>. Each element of the array is of type <b>VT_BSTR</b> and contains the name of a scope to which the current client is assigned. The number of elements in the array is specified by the <i>PageSize</i> parameter.

## -returns

If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If multiple threads access the same authorization store, a call to the  <b>GetAssignedScopesPage</b> method on one of the threads might not return accurate results if the other thread modifies the store.

In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> values must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.