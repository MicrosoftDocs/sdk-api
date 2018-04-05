---
UID: NN:vds.IVdsHwProviderType
title: IVdsHwProviderType
author: windows-driver-content
description: Provides a method to retrieve the type of hardware provider.
old-location: base\ivdshwprovidertype.htm
old-project: VDS
ms.assetid: 24bd634e-96e1-4f2a-a70b-3aae734c75f9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsHwProviderType, IVdsHwProviderType interface [VDS], IVdsHwProviderType interface [VDS], described, base.ivdshwprovidertype, vds/IVdsHwProviderType, vdshwprv/IVdsHwProviderType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsHwProviderType
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsHwProviderType interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to retrieve the type of hardware provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHwProviderType</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsHwProviderType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHwProviderType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e88fd2df-531d-46d8-a91b-9b9f8578e57b">GetProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the type of the hardware provider.</p> (Inherited from <b>IVdsHwProviderType</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/131e927d-d32a-44f6-8aae-28839cfa9e7d">Provider Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

