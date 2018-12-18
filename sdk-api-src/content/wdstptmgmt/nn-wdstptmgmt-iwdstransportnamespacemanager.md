---
UID: NN:wdstptmgmt.IWdsTransportNamespaceManager
title: IWdsTransportNamespaceManager
author: windows-sdk-content
description: Manages namespaces on a WDS transport server.
old-location: wds\iwdstransportnamespacemanager.htm
tech.root: wds
ms.assetid: de5fc470-af9f-4f9f-bc17-a347dc702e36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWdsTransportNamespaceManager, IWdsTransportNamespaceManager interface [Windows Deployment Services], IWdsTransportNamespaceManager interface [Windows Deployment Services],described, wds.iwdstransportnamespacemanager, wdstptmgmt/IWdsTransportNamespaceManager
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportNamespaceManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportNamespaceManager interface


## -description


Manages namespaces on a WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespaceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWdsTransportNamespaceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportNamespaceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fda205d6-f99a-4fec-96bb-0e37e9ca16ce">CreateNamespace</a>
</td>
<td align="left" width="63%">
Creates a namespace object that can be registered on the WDS transport server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8afe8d0c-4c6b-45a6-a330-b2cee59ca1ad">RetrieveNamespace</a>
</td>
<td align="left" width="63%">
Retrieves,  by name, a namespace object that is registered with the WDS transport server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3151ab6b-7ceb-4ecc-8480-cb5f9700ca9a">RetrieveNamespaces</a>
</td>
<td align="left" width="63%">
Retrieves a collection of namespace objects that represent namespaces on the server that match specified criteria.

</td>
</tr>
</table> 

