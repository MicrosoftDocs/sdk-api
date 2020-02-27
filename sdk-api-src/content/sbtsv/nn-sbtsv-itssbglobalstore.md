---
UID: NN:sbtsv.ITsSbGlobalStore
title: ITsSbGlobalStore (sbtsv.h)
description: Exposes methods that query for target computers, sessions, environments, and farms that have been added to the Remote Desktop Connection Broker (RD Connection Broker) store.
old-location: termserv\itssbglobalstore.htm
tech.root: TermServ
ms.assetid: d25b6f73-ee5f-40e4-9c49-fd48dd3990d2
ms.date: 12/05/2018
ms.keywords: ITsSbGlobalStore, ITsSbGlobalStore interface [Remote Desktop Services], ITsSbGlobalStore interface [Remote Desktop Services],described, sbtsv/ITsSbGlobalStore, termserv.itssbglobalstore
f1_keywords:
- sbtsv/ITsSbGlobalStore
dev_langs:
- c++
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
- sbtsv.h
api_name:
- ITsSbGlobalStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbGlobalStore interface


## -description


Exposes methods that query for target computers, sessions, environments, and farms that have been added 
to the Remote Desktop Connection Broker (RD Connection Broker) store. Plug-ins can obtain an instance of the global store from the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a> 
object that they retrieve during initialization.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbGlobalStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbGlobalStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbGlobalStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-enumerateenvironmentsbyprovider">EnumerateEnvironmentsByProvider</a>
</td>
<td align="left" width="63%">
Returns an array that contains the environments present on the specified provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-enumeratefarms">EnumerateFarms</a>
</td>
<td align="left" width="63%">
Enumerates all the farms that have been added by the specified resource 
plug-in. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-enumeratesessions">EnumerateSessions</a>
</td>
<td align="left" width="63%">
Returns an array that contains sessions on the specified provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-enumeratetargets">EnumerateTargets</a>
</td>
<td align="left" width="63%">
Returns an array that contains the specified targets present in the global store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-getfarmproperty">GetFarmProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property of a farm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-querysessionbysessionid">QuerySessionBySessionId</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession">ITsSbSession</a> object associated with the given 
session ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbglobalstore-querytarget">QueryTarget</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object for the given parameters.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

