---
UID: NN:vdshwprv.IVdsProviderPrivate
title: IVdsProviderPrivate
author: windows-driver-content
description: Provides methods to enable VDS to perform miscellaneous operations on provider objects.
old-location: base\ivdsproviderprivate.htm
old-project: VDS
ms.assetid: 5f1c38bf-85a7-4123-becb-e8abf3052b41
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsProviderPrivate, IVdsProviderPrivate interface [VDS], IVdsProviderPrivate interface [VDS], described, base.ivdsproviderprivate, vdshwprv/IVdsProviderPrivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsProviderPrivate
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsProviderPrivate interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to enable VDS to perform miscellaneous operations on provider objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProviderPrivate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsProviderPrivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProviderPrivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f346255-c5c6-4ca3-9718-0347c3f8294a">GetObject</a>
</td>
<td align="left" width="63%">
Returns the specified VDS object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5b2ac78-6a23-470c-a762-26ce6358e0b6">OnLoad</a>
</td>
<td align="left" width="63%">
Prompts the provider to initialize itself, and passes a callback object that the provider uses to get necessary interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c4b2a0b-f056-4d3f-976c-0339c930e3cf">OnUnload</a>
</td>
<td align="left" width="63%">
Prompts the provider to uninitialize itself.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

