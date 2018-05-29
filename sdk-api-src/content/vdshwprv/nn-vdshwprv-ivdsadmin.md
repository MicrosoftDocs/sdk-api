---
UID: NN:vdshwprv.IVdsAdmin
title: IVdsAdmin
author: windows-sdk-content
description: Registers providers with VDS.
old-location: base\ivdsadmin.htm
old-project: VDS
ms.assetid: 693ee0c0-9f86-4f78-9724-f3a3420463c9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsAdmin, IVdsAdmin interface [VDS], IVdsAdmin interface [VDS],described, base.ivdsadmin, vdshwprv/IVdsAdmin
ms.prod: windows
ms.technology: windows-sdk
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
-	IVdsAdmin
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAdmin interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Registers providers with VDS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAdmin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsAdmin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAdmin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb6e0037-7f44-418d-897c-12bf15224841">RegisterProvider</a>
</td>
<td align="left" width="63%">
Registers the specified provider with VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da78b4ed-17e3-4953-9e5e-310e55349058">UnregisterProvider</a>
</td>
<td align="left" width="63%">
Deletes VDS provider registration data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

