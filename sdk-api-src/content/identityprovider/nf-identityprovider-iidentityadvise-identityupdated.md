---
UID: NF:identityprovider.IIdentityAdvise.IdentityUpdated
title: IIdentityAdvise::IdentityUpdated (identityprovider.h)
description: Is called by an identity provider to notify a calling application that an identity event occurred.
helpviewer_keywords: ["IDENTITY_ASSOCIATED","IDENTITY_CONNECTED","IDENTITY_CREATED","IDENTITY_DELETED","IDENTITY_DISASSOCIATED","IDENTITY_DISCONNECTED","IDENTITY_IMPORTED","IDENTITY_PROPCHANGE","IIdentityAdvise interface [Security]","IdentityUpdated method","IIdentityAdvise.IdentityUpdated","IIdentityAdvise::IdentityUpdated","IdentityUpdated","IdentityUpdated method [Security]","IdentityUpdated method [Security]","IIdentityAdvise interface","identityprovider/IIdentityAdvise::IdentityUpdated","identitystore/IIdentityAdvise::IdentityUpdated","security.iidentityadvise_identityupdated"]
old-location: security\iidentityadvise_identityupdated.htm
tech.root: security
ms.assetid: c41ca389-eac9-4c74-b0e7-950cd21f2199
ms.date: 12/05/2018
ms.keywords: IDENTITY_ASSOCIATED, IDENTITY_CONNECTED, IDENTITY_CREATED, IDENTITY_DELETED, IDENTITY_DISASSOCIATED, IDENTITY_DISCONNECTED, IDENTITY_IMPORTED, IDENTITY_PROPCHANGE, IIdentityAdvise interface [Security],IdentityUpdated method, IIdentityAdvise.IdentityUpdated, IIdentityAdvise::IdentityUpdated, IdentityUpdated, IdentityUpdated method [Security], IdentityUpdated method [Security],IIdentityAdvise interface, identityprovider/IIdentityAdvise::IdentityUpdated, identitystore/IIdentityAdvise::IdentityUpdated, security.iidentityadvise_identityupdated
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identitystore.idl
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
 - IIdentityAdvise::IdentityUpdated
 - identityprovider/IIdentityAdvise::IdentityUpdated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IdentityProvider.h
 - Identitystore.h
api_name:
 - IIdentityAdvise.IdentityUpdated
---

# IIdentityAdvise::IdentityUpdated


## -description

The <b>IdentityUpdated</b> method is called by an identity provider to notify a calling application that an identity event occurred. An application calls the <a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">IIdentityProvider::Advise</a> method to specify events for which it is to be notified.

## -parameters

### -param dwIdentityUpdateEvents [in]

The identity events that occurred. The value of this parameter can be zero or more of the following values combined by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_ASSOCIATED"></a><a id="identity_associated"></a><dl>
<dt><b>IDENTITY_ASSOCIATED</b></dt>
<dt>0X0001</dt>
</dl>
</td>
<td width="60%">
An identity was associated with the identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DISASSOCIATED"></a><a id="identity_disassociated"></a><dl>
<dt><b>IDENTITY_DISASSOCIATED</b></dt>
<dt>0X0002</dt>
</dl>
</td>
<td width="60%">
An identity was disassociated from the identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_CREATED"></a><a id="identity_created"></a><dl>
<dt><b>IDENTITY_CREATED</b></dt>
<dt>0X0004</dt>
</dl>
</td>
<td width="60%">
A new identity was created.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_IMPORTED"></a><a id="identity_imported"></a><dl>
<dt><b>IDENTITY_IMPORTED</b></dt>
<dt>0X0008</dt>
</dl>
</td>
<td width="60%">
An identity was imported from another identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DELETED"></a><a id="identity_deleted"></a><dl>
<dt><b>IDENTITY_DELETED</b></dt>
<dt>0X0010</dt>
</dl>
</td>
<td width="60%">
An identity was deleted from the identity store.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_PROPCHANGE"></a><a id="identity_propchange"></a><dl>
<dt><b>IDENTITY_PROPCHANGE</b></dt>
<dt>0X0020</dt>
</dl>
</td>
<td width="60%">
The value of  a property of an identity changed.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_CONNECTED"></a><a id="identity_connected"></a><dl>
<dt><b>IDENTITY_CONNECTED</b></dt>
<dt>0X0040</dt>
</dl>
</td>
<td width="60%">
The identity is a connected identity.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DISCONNECTED"></a><a id="identity_disconnected"></a><dl>
<dt><b>IDENTITY_DISCONNECTED</b></dt>
<dt>0X0080</dt>
</dl>
</td>
<td width="60%">
The identity was disconnected from the identity provider.

</td>
</tr>
</table>

### -param lpszUniqueID [in]

The identity associated with the events that occurred.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityadvise">IIdentityAdvise</a>