---
UID: NN:vdshwprv.IVdsHwProviderPrivate
title: IVdsHwProviderPrivate
author: windows-sdk-content
description: Provides a method that enables VDS to determine whether the hardware provider manages a specified LUN.
old-location: base\ivdshwproviderprivate.htm
tech.root: VDS
ms.assetid: 7e6dbf9e-9060-46bf-be11-9d9d640a3d36
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsHwProviderPrivate, IVdsHwProviderPrivate interface [VDS], IVdsHwProviderPrivate interface [VDS],described, base.ivdshwproviderprivate, vdshwprv/IVdsHwProviderPrivate
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
 - IVdsHwProviderPrivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsHwProviderPrivate interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method that enables VDS to determine whether the hardware provider manages a specified LUN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderPrivate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsHwProviderPrivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderPrivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06ba3486-9381-4898-b639-3d94b83be857">QueryIfCreatedLun</a>
</td>
<td align="left" width="63%">
Enables VDS to determine whether the hardware provider manages the specified LUN.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

