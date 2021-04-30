---
UID: NF:identityprovider.IIdentityProvider.Advise
title: IIdentityProvider::Advise (identityprovider.h)
description: Allows a calling application to specify the list of identity events for which the application is to be notified.
helpviewer_keywords: ["Advise","Advise method [Security]","Advise method [Security]","IIdentityProvider interface","IDENTITY_ASSOCIATED","IDENTITY_CREATED","IDENTITY_DELETED","IDENTITY_DISASSOCIATED","IDENTITY_IMPORTED","IDENTITY_PROPCHANGE","IIdentityProvider interface [Security]","Advise method","IIdentityProvider.Advise","IIdentityProvider::Advise","identityprovider/IIdentityProvider::Advise","security.iidentityprovider_advise"]
old-location: security\iidentityprovider_advise.htm
tech.root: security
ms.assetid: fcac9d30-64ed-4746-aacc-ee659c2b2642
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Security], Advise method [Security],IIdentityProvider interface, IDENTITY_ASSOCIATED, IDENTITY_CREATED, IDENTITY_DELETED, IDENTITY_DISASSOCIATED, IDENTITY_IMPORTED, IDENTITY_PROPCHANGE, IIdentityProvider interface [Security],Advise method, IIdentityProvider.Advise, IIdentityProvider::Advise, identityprovider/IIdentityProvider::Advise, security.iidentityprovider_advise
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Identityprovider.idl
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
 - IIdentityProvider::Advise
 - identityprovider/IIdentityProvider::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.Advise
---

# IIdentityProvider::Advise


## -description

The <b>Advise</b> method allows a calling application to specify the list of identity events for which the application is to be  notified.

## -parameters

### -param pIdentityAdvise [in]

A pointer to the <a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityadvise">IIdentityAdvise</a> interface implemented by the calling application. This interface provides a method that the identity provider can call when one of the events specified by the <i>dwIdentityUpdateEvents</i> parameter occurs.

### -param dwIdentityUpdateEvents [in]

The identity events for which the calling application is to be notified. The value of this parameter can be zero or more of the following values combined by using a bitwise-<b>OR</b> operation.

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
</table>

### -param pdwCookie [out]

A pointer to a value that identifies this connection. When you have finished using this connection, delete it by passing this value to the <a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-unadvise">UnAdvise</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/identityprovider/nf-identityprovider-iidentityadvise-identityupdated">IIdentityAdvise::IdentityUpdated</a>



<a href="/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>