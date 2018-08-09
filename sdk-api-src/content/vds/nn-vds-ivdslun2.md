---
UID: NN:vds.IVdsLun2
title: IVdsLun2
author: windows-sdk-content
description: Provides methods for applying and querying logical unit number (LUN) hints.
old-location: base\ivdslun2.htm
old-project: vds
ms.assetid: 1cc26b91-d77b-4f8d-8c01-40b58cb03038
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsLun2, IVdsLun2 interface, IVdsLun2 interface,described, base.ivdslun2, vds/IVdsLun2, vdshwprv/IVdsLun2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLun2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLun2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for applying and querying logical unit number (LUN) hints.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLun2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLun2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLun2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0032dce3-876c-4a02-8e06-203b3f83ca08">ApplyHints2</a>
</td>
<td align="left" width="63%">
Applies a new set of 
   hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes. This method is identical to the <a href="https://msdn.microsoft.com/2582913a-bc13-45dc-b0c8-9429945014da">IVdsLun::ApplyHints</a> method, except that it uses a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure instead of a <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/077d200a-2eab-4dbe-b7b9-873061fa2c4b">QueryHints2</a>
</td>
<td align="left" width="63%">
Returns the hints 
   currently applied to the LUN. This method is identical to the <a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a> method, except that it uses a <a href="https://msdn.microsoft.com/e24935ac-17c8-4338-99cb-2408ca61da8a">VDS_HINTS2</a> structure instead of a <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.

</td>
</tr>
</table> 

