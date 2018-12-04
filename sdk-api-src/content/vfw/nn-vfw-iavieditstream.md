---
UID: NN:vfw.IAVIEditStream
title: IAVIEditStream
author: windows-sdk-content
description: The IAVIEditStream interface supports manipulating and modifying editable streams. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:\_
The IAVIEditStream interface supports manipulating and modifying editable streams. Uses IUnknown::QueryInterface, IUnknown::AddRef, IUnknown::Release in addition to the following custom methods:
old-location: multimedia\iavieditstream.htm
tech.root: Multimedia
ms.assetid: d32dc386-05cf-4f7b-9785-a38586a09402
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IAVIEditStream, IAVIEditStream interface [Windows Multimedia], IAVIEditStream interface [Windows Multimedia],described, _win32_IAVIEditStream, multimedia.iavieditstream, vfw/IAVIEditStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIEditStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIEditStream interface


## -description



The <b>IAVIEditStream</b> interface supports manipulating and modifying editable streams. Uses <a href="https://msdn.microsoft.com/6db0af58-51ee-499a-81c4-4bce8aae0f06">IUnknown::QueryInterface</a>, <a href="https://msdn.microsoft.com/14ffd2ab-ac0c-4de7-adb8-4fe800c9bda9">IUnknown::AddRef</a>, <a href="https://msdn.microsoft.com/61d760e3-72bf-462e-bfd5-5578b53860ba">IUnknown::Release</a> in addition to the following custom methods:




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAVIEditStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAVIEditStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAVIEditStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7112056e-5e25-4262-abe3-5cbb0675a475">Clone</a>
</td>
<td align="left" width="63%">
Duplicates a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2012d04-4fe5-4a49-8160-d27b7bc1bfc8">Copy</a>
</td>
<td align="left" width="63%">
Copies a stream or a portion of it to a temporary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e889d435-5c33-402d-bd69-c9122670e404">Cut</a>
</td>
<td align="left" width="63%">
Removes a portion of a stream and places it in a temporary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdb6de96-6a1e-49ca-a824-ed6d7b43fd13">Paste</a>
</td>
<td align="left" width="63%">
Copies a stream or a portion of it and places it in another stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46496c24-cbe0-4234-8683-f39fa58e076b">SetInfo</a>
</td>
<td align="left" width="63%">
Changes the characteristics of a stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

