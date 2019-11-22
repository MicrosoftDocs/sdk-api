---
UID: NN:objidlbase.IServerSecurity
title: IServerSecurity (objidlbase.h)

description: Used by a server to help authenticate the client and to manage impersonation of the client.
old-location: com\iserversecurity.htm
tech.root: com
ms.assetid: aacef77c-7185-44ed-aa1a-465c6100a431

ms.date: 12/05/2018
ms.keywords: IServerSecurity, IServerSecurity interface [COM], IServerSecurity interface [COM],described, _com_iserversecurity, com.iserversecurity, objidlbase/IServerSecurity
ms.topic: interface
f1_keywords: 
 - "objidlbase/IServerSecurity"
dev_langs:
 - c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IServerSecurity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServerSecurity interface


## -description


Used by a server to help authenticate the client and to manage impersonation of the client. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServerSecurity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServerSecurity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServerSecurity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">ImpersonateClient</a>
</td>
<td align="left" width="63%">
Enables a server to impersonate a client for the duration of a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iserversecurity-isimpersonating">IsImpersonating</a>
</td>
<td align="left" width="63%">
Indicates whether the server is currently impersonating the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iserversecurity-queryblanket">QueryBlanket</a>
</td>
<td align="left" width="63%">
Retrieves information about the client that invoked one of the server's methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">RevertToSelf</a>
</td>
<td align="left" width="63%">
Restores the authentication information of a thread to what it was before impersonation began.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coswitchcallcontext">CoSwitchCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/com/security-in-com">Security in COM</a>
 

 

