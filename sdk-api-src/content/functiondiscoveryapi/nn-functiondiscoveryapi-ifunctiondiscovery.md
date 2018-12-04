---
UID: NN:functiondiscoveryapi.IFunctionDiscovery
title: IFunctionDiscovery
author: windows-sdk-content
description: This interface is used by client programs to discover function instances, get the default function instance for a category, and create advanced Function Discovery query objects that enable registering Function Discovery defaults, among other things.
old-location: ncd\ifunctiondiscovery.htm
tech.root: fundisc
ms.assetid: 352a8d61-7d3a-423d-8b7e-1163d4fa1e00
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFunctionDiscovery, IFunctionDiscovery interface, IFunctionDiscovery interface,described, functiondiscoveryapi/IFunctionDiscovery, ncd.ifunctiondiscovery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionDiscovery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscovery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface is used by client programs to discover function instances, get the default function instance for a category, and create advanced Function Discovery query objects that enable registering Function Discovery defaults, among other things.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionDiscovery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionDiscovery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionDiscovery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a99213b5-b310-4ce2-99ca-07b343f08c4d">AddInstance</a>
</td>
<td align="left" width="63%">
Creates or modifies a function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">CreateInstanceCollectionQuery</a>
</td>
<td align="left" width="63%">
Creates a query for a collection of specific function instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80e70972-ced1-416e-aa4f-69c54b2cbf95">CreateInstanceQuery</a>
</td>
<td align="left" width="63%">
Creates a query for a specific function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f3b2517-0acf-4a43-9539-d905c78be426">GetInstance</a>
</td>
<td align="left" width="63%">
Gets the specified function instance, based on identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/615d252c-7365-4ef5-9e4f-94a49783a1bb">GetInstanceCollection</a>
</td>
<td align="left" width="63%">
Gets the specified collection of function instances, based on category and subcategory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/743ec310-ea35-4c4b-92f0-bbfe0a2f6f30">RemoveInstance</a>
</td>
<td align="left" width="63%">
Removes the specified function instance, based on category and subcategory.

</td>
</tr>
</table> 

