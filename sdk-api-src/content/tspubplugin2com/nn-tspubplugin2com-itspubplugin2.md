---
UID: NN:tspubplugin2com.ItsPubPlugin2
title: ItsPubPlugin2 (tspubplugin2com.h)
description: Specifies methods that provide information about resources available to users of RemoteApp and Desktop Connections.
old-location: termserv\itspubplugin2.htm
tech.root: TermServ
ms.assetid: 1ef27b3a-b897-4757-803d-d3a18959895c
ms.date: 12/05/2018
ms.keywords: ItsPubPlugin2, ItsPubPlugin2 interface [Remote Desktop Services], ItsPubPlugin2 interface [Remote Desktop Services],described, termserv.itspubplugin2, tspubplugin2com/ItsPubPlugin2
f1_keywords:
- tspubplugin2com/ItsPubPlugin2
dev_langs:
- c++
req.header: tspubplugin2com.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tspubplugin2com.idl
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
- tspubplugin2com.h
api_name:
- ItsPubPlugin2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ItsPubPlugin2 interface


## -description


Specifies methods that provide information about resources available to users of RemoteApp and Desktop Connections. This interface is an enhancement to the <a href="https://docs.microsoft.com/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin">ItsPubPlugin</a> interface.

The methods in this interface are called by the RemoteApp and Desktop Connection Management service in Remote Desktop Web Access (RD Web Access) and Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ItsPubPlugin2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin">ItsPubPlugin</a>. <b>ItsPubPlugin2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ItsPubPlugin2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-deletepersonaldesktopassignment">DeletePersonalDesktopAssignment</a>
</td>
<td align="left" width="63%">
Called to delete a mapping between the specified user and a virtual machine in a personal virtual desktop collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-getresource2">GetResource2</a>
</td>
<td align="left" width="63%">
This method is reserved and should always return <b>E_NOTIMPL</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-getresource2list">GetResource2List</a>
</td>
<td align="left" width="63%">
Retrieves a list of resources assigned to the specified user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tspubplugin2com/nf-tspubplugin2com-itspubplugin2-resolvepersonaldesktop">ResolvePersonalDesktop</a>
</td>
<td align="left" width="63%">
Called to resolve a mapping between the specified user and a virtual machine in a personal virtual desktop collection.

</td>
</tr>
</table> 

