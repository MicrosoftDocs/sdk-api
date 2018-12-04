---
UID: NN:functiondiscoveryapi.IFunctionInstance
title: IFunctionInstance
author: windows-sdk-content
description: A function instance is created as the result of calling one of the IFunctionDiscovery methods; client program do not create these objects themselves.
old-location: ncd\ifunctioninstance.htm
tech.root: fundisc
ms.assetid: cc421719-73a6-4d4d-9bf8-171e46c4e275
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFunctionInstance, IFunctionInstance interface, IFunctionInstance interface,described, functiondiscoveryapi/IFunctionInstance, ncd.ifunctioninstance
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
 - IFunctionInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstance interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

    A function instance is created as the result of calling one of the <a href="https://msdn.microsoft.com/352a8d61-7d3a-423d-8b7e-1163d4fa1e00">IFunctionDiscovery</a>  methods; client program do not create these objects themselves.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstance</b> interface inherits from <b>IServiceProvider</b>. <b>IFunctionInstance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb5f144-c9b0-455e-aff9-0c07225a21f6">GetCategory</a>
</td>
<td align="left" width="63%">
Gets the category and subcategory strings for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a198bc4-cdec-4d46-a1a2-3952d4dc2a7d">GetID</a>
</td>
<td align="left" width="63%">
Gets the identifier string for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fad5e3f0-a440-4b09-ba8c-04bae2d14a2a">GetProviderInstanceID</a>
</td>
<td align="left" width="63%">
Gets the identifier string for the provider instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">OpenPropertyStore</a>
</td>
<td align="left" width="63%">
Opens the property store for the function instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">QueryService</a>
</td>
<td align="left" width="63%">
Acts as the factory method for any services exposed through an implementation of <b>IFunctionInstance</b>.

</td>
</tr>
</table> 

