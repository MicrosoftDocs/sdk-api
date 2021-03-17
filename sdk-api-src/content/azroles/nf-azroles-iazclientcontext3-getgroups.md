---
UID: NF:azroles.IAzClientContext3.GetGroups
title: IAzClientContext3::GetGroups (azroles.h)
description: Returns an array of the application groups associated with this client context.
helpviewer_keywords: ["AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY","GetGroups","GetGroups method [Security]","GetGroups method [Security]","IAzClientContext3 interface","IAzClientContext3 interface [Security]","GetGroups method","IAzClientContext3.GetGroups","IAzClientContext3::GetGroups","azroles/IAzClientContext3::GetGroups","security.iazclientcontext3_getgroups"]
old-location: security\iazclientcontext3_getgroups.htm
tech.root: security
ms.assetid: e34b55e1-df7f-4356-b84e-8f297afcda24
ms.date: 12/05/2018
ms.keywords: AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY, GetGroups, GetGroups method [Security], GetGroups method [Security],IAzClientContext3 interface, IAzClientContext3 interface [Security],GetGroups method, IAzClientContext3.GetGroups, IAzClientContext3::GetGroups, azroles/IAzClientContext3::GetGroups, security.iazclientcontext3_getgroups
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzClientContext3::GetGroups
 - azroles/IAzClientContext3::GetGroups
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.GetGroups
---

# IAzClientContext3::GetGroups


## -description

The <b>GetGroups</b> method returns an array of the application groups associated with this client context.

## -parameters

### -param bstrScopeName [in]

The name of the scope in which to check for application groups. This parameter is ignored if the value of the ulOptions parameter is set to <b>AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY</b>.

### -param ulOptions [in]

A set of flags that modify the behavior of this method. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY"></a><a id="az_client_context_get_groups_store_level_only"></a><dl>
<dt><b>AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
This method checks only for application groups at the store level.

</td>
</tr>
</table>

### -param pGroupArray [out]

A pointer to an array of the names of application groups associated with this client context.

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the  JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains the name of an application group.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext3">IAzClientContext3</a>