---
UID: NN:vdshwprv.IVdsHwProviderPrivateMpio
title: IVdsHwProviderPrivateMpio
author: windows-sdk-content
description: Provides a method that sets the status of paths originating from a particular HBA port to the provider.
old-location: base\ivdshwproviderprivatempio.htm
tech.root: VDS
ms.assetid: fa60e832-1148-4ffb-bf70-bd7b27180cdd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsHwProviderPrivateMpio, IVdsHwProviderPrivateMpio interface [VDS], IVdsHwProviderPrivateMpio interface [VDS],described, base.ivdshwproviderprivatempio, vdshwprv/IVdsHwProviderPrivateMpio
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsHwProviderPrivateMpio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsHwProviderPrivateMpio interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method that sets the status of paths originating from a particular HBA port to the provider.
  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderPrivateMpio</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsHwProviderPrivateMpio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderPrivateMpio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc25ca9-7cb4-438c-b9da-4bf93bd18a0c">SetAllPathStatusesFromHbaPort</a>
</td>
<td align="left" width="63%">
Sets the statuses of paths originating from a particular HBA port to a specified status.</p> (Inherited from <b>IVdsHwProviderPrivateMpio</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cc30a78a-78a4-49c2-a97d-228400da46a9">IVdsController</a>



<a href="https://msdn.microsoft.com/1fc25ca9-7cb4-438c-b9da-4bf93bd18a0c">SetAllPathStatusesFromHbaPort</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

