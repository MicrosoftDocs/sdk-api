---
UID: NN:functiondiscoveryprovider.IProviderPublishing
title: IProviderPublishing (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Is implemented by a discovery provider to enable a client program to add and remove function instances.
old-location: ncd\iproviderpublishing.htm
tech.root: FunDisc
ms.assetid: 7647db1b-88c8-44f3-b2af-a61dad4790f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProviderPublishing, IProviderPublishing interface, IProviderPublishing interface,described, functiondiscoveryprovider/IProviderPublishing, ncd.iproviderpublishing
ms.topic: interface
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderPublishing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProviderPublishing interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is implemented by a discovery provider to enable a client program to add and remove function instances.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderPublishing</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProviderPublishing</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProviderPublishing</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c8988d0-552a-434b-b33c-31017a191896">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b4f6122-944e-4fe9-be95-dd09ae1542f1">RemoveInstance</a>
</td>
<td align="left" width="63%">
Deletes an existing function instance.

</td>
</tr>
</table> 


## -remarks



Clients access the function instance through <a href="https://msdn.microsoft.com/a99213b5-b310-4ce2-99ca-07b343f08c4d">IFunctionDiscovery::AddInstance</a> and <a href="https://msdn.microsoft.com/743ec310-ea35-4c4b-92f0-bbfe0a2f6f30">IFunctionDiscovery::RemoveInstance</a>.

The <b>IProviderPublishing</b> interface can only be implemented by discovery providers that support category change notification. At this time only PnP providers support change notification.



