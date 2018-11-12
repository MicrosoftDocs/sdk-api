---
UID: NF:identityprovider.IIdentityProvider.Advise
title: IIdentityProvider::Advise
author: windows-sdk-content
description: Allows a calling application to specify the list of identity events for which the application is to be notified.
old-location: security\iidentityprovider_advise.htm
tech.root: secauthn
ms.assetid: fcac9d30-64ed-4746-aacc-ee659c2b2642
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Advise, Advise method [Security], Advise method [Security],IIdentityProvider interface, IDENTITY_ASSOCIATED, IDENTITY_CREATED, IDENTITY_DELETED, IDENTITY_DISASSOCIATED, IDENTITY_IMPORTED, IDENTITY_PROPCHANGE, IIdentityProvider interface [Security],Advise method, IIdentityProvider.Advise, IIdentityProvider::Advise, identityprovider/IIdentityProvider::Advise, security.iidentityprovider_advise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Identityprovider.h
api_name:
 - IIdentityProvider.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdentityProvider::Advise


## -description


The <b>Advise</b> method allows a calling application to specify the list of identity events for which the application is to be  notified.


## -parameters




### -param pIdentityAdvise [in]

A pointer to the <a href="https://msdn.microsoft.com/fa348d46-bcd2-4009-89d6-11e738d4a82b">IIdentityAdvise</a> interface implemented by the calling application. This interface provides a method that the identity provider can call when one of the events specified by the <i>dwIdentityUpdateEvents</i> parameter occurs.


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

A pointer to a value that identifies this connection. When you have finished using this connection, delete it by passing this value to the <a href="https://msdn.microsoft.com/ba8a12fc-ea4c-45b5-8339-9cbc88c160db">UnAdvise</a> method.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/c41ca389-eac9-4c74-b0e7-950cd21f2199">IIdentityAdvise::IdentityUpdated</a>



<a href="https://msdn.microsoft.com/0f23e369-1501-4e72-94d1-dadb9dac5be6">IIdentityProvider</a>
 

 

