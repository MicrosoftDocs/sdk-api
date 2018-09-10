---
UID: NN:rometadataapi.IMetaDataDispenser
title: IMetaDataDispenser
author: windows-sdk-content
description: Provides methods to create a new metadata scope, or open an existing one.
old-location: winrt\imetadatadispenser.htm
tech.root: WinRT
ms.assetid: 3454193d-9068-4032-ae9e-b3087509b0b8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMetaDataDispenser, IMetaDataDispenser interface [Windows Runtime], IMetaDataDispenser interface [Windows Runtime],described, rometadataapi/IMetaDataDispenser, winrt.imetadatadispenser
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataDispenser interface


## -description


Provides methods to create a new metadata scope, or open an existing one.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataDispenser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMetaDataDispenser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataDispenser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b7a5e73-e7ef-427a-baa4-3f0defd566a3">DefineScope</a>
</td>
<td align="left" width="63%">
Creates a new area in memory in which you can create new metadata.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77ba5ee6-082c-478f-83fc-7f6c31ee3c74">OpenScope</a>
</td>
<td align="left" width="63%">
Opens an existing, on-disk file and maps its metadata into memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4558b229-0fe9-4ff7-a666-e69b47cb8170">OpenScopeOnMemory</a>
</td>
<td align="left" width="63%">
Opens an area of memory that contains existing metadata. 

</td>
</tr>
</table> 

