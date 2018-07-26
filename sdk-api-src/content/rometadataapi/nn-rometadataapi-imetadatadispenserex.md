---
UID: NN:rometadataapi.IMetaDataDispenserEx
title: IMetaDataDispenserEx
author: windows-sdk-content
description: Extends the IMetaDataDispenser interface to provide the capability to control how the metadata APIs operate on the current metadata scope.
old-location: winrt\imetadatadispenserex.htm
old-project: WinRT
ms.assetid: b61c8d05-6d73-4f84-95b2-2a892f3de77c
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IMetaDataDispenserEx, IMetaDataDispenserEx interface [Windows Runtime], IMetaDataDispenserEx interface [Windows Runtime],described, rometadataapi/IMetaDataDispenserEx, winrt.imetadatadispenserex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataDispenserEx interface


## -description


Extends the <a href="https://msdn.microsoft.com/3454193d-9068-4032-ae9e-b3087509b0b8">IMetaDataDispenser</a> interface to provide the capability to control how the metadata APIs operate on the current metadata scope.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataDispenserEx</b> interface inherits from <b>IMetaDataDispenser</b>. <b>IMetaDataDispenserEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataDispenserEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f691157-9f3d-4e04-91ee-9d62c23569d8">FindAssembly</a>
</td>
<td align="left" width="63%">
Gets the name of the assembly.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/258d670b-6a94-4151-8746-a3df69677c5b">FindAssemblyModule</a>
</td>
<td align="left" width="63%">
Finds the name of the assembly module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f061c7f-bcb8-4b1e-b84b-0398f08a6d69">GetCORSystemDirectory</a>
</td>
<td align="left" width="63%">
Gets the directory that holds the current common language runtime (CLR). This method is supported only for use by out-of-process debuggers. If called from another component, it will return E_NOTIMPL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451273">GetOption</a>
</td>
<td align="left" width="63%">
Gets the value of the specified option for the current metadata scope. The option controls how calls to the current metadata scope are handled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e76d295a-bce9-42c2-9a9b-a4d31741f47f">OpenScopeOnITypeInfo</a>
</td>
<td align="left" width="63%">
Opens the specified scope type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb84abf1-0bba-4f9d-98fb-3ed67819a9dc">SetOption</a>
</td>
<td align="left" width="63%">
Sets the specified option to a given value for the current metadata scope. The option controls how calls to the current metadata scope are handled.

</td>
</tr>
</table> 

