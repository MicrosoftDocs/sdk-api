---
UID: NN:objidl.IServerSecurity
title: IServerSecurity
author: windows-sdk-content
description: Used by a server to help authenticate the client and to manage impersonation of the client.
old-location: com\iserversecurity.htm
old-project: com
ms.assetid: aacef77c-7185-44ed-aa1a-465c6100a431
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IServerSecurity, IServerSecurity interface [COM], IServerSecurity interface [COM],described, _com_iserversecurity, com.iserversecurity, objidlbase/IServerSecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IServerSecurity
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IServerSecurity interface


## -description


Used by a server to help authenticate the client and to manage impersonation of the client. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServerSecurity</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IServerSecurity</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/20398b63-0fcb-40ab-93ed-f4c75760eb9e">ImpersonateClient</a>
</td>
<td align="left" width="63%">
Enables a server to impersonate a client for the duration of a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f847348a-1785-4b4a-b43e-a5eea21847c4">IsImpersonating</a>
</td>
<td align="left" width="63%">
Indicates whether the server is currently impersonating the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868">QueryBlanket</a>
</td>
<td align="left" width="63%">
Retrieves information about the client that invoked one of the server's methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21952f54-439e-446f-a206-4b35759b1090">RevertToSelf</a>
</td>
<td align="left" width="63%">
Restores the authentication information of a thread to what it was before impersonation began.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/146855a2-97ec-4e71-88dc-316eaa1a24a0">CoSwitchCallContext</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

