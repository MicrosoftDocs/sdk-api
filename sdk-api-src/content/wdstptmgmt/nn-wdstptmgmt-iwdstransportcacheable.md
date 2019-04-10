---
UID: NN:wdstptmgmt.IWdsTransportCacheable
title: IWdsTransportCacheable (wdstptmgmt.h)
author: windows-sdk-content
description: Provides caching for objects that handle persistent data. This interface can be inherited by other interfaces that represent persisted objects.
old-location: wds\iwdstransportcacheable.htm
tech.root: wds
ms.assetid: 2245d198-056c-467f-aae7-b1bb02f188e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportCacheable, IWdsTransportCacheable interface [Windows Deployment Services], IWdsTransportCacheable interface [Windows Deployment Services],described, wds.iwdstransportcacheable, wdstptmgmt/IWdsTransportCacheable
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
 - IWdsTransportCacheable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportCacheable interface


## -description


Provides caching for objects that handle persistent data. This interface can be inherited by other interfaces that represent persisted objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportCacheable</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWdsTransportCacheable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportCacheable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd651e56-3945-48ca-a490-e20db88eb2fb">Commit</a>
</td>
<td align="left" width="63%">
Commits object data members to the underlying data store if the <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property has been set. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c8495b9-6c76-4bb0-8237-5f9008cefc91">Discard</a>
</td>
<td align="left" width="63%">
Discards all changes made to the object data members by clearing the <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property and then calling the object's <a href="https://msdn.microsoft.com/2fd838b5-5623-4133-9ad8-ec051b2b698d">IWdsTransportCacheable::Refresh</a> method to reread the current object data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fd838b5-5623-4133-9ad8-ec051b2b698d">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the object data members by rereading their values from the underlying data store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportCacheable</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">Dirty</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates whether object data has been modified. 

</td>
</tr>
</table> 

