---
UID: NN:msctf.ITfContextOwnerServices
title: ITfContextOwnerServices
author: windows-sdk-content
description: The ITfContextOwnerServices interface is implemented by the manager and used by a text service or application acting as context owners.
old-location: tsf\itfcontextownerservices.htm
tech.root: TSF
ms.assetid: fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfContextOwnerServices, ITfContextOwnerServices interface [Text Services Framework], ITfContextOwnerServices interface [Text Services Framework],described, _tsf_itfcontextownerservices_ref, msctf/ITfContextOwnerServices, tsf.itfcontextownerservices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwnerServices interface


## -description


The <b>ITfContextOwnerServices</b> interface is implemented by the manager and used by a text service or application acting as context owners. The interface provides notification changes to sinks and other services to context owners that do not implement the <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> or <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a> interfaces. Clients obtain this interface by calling the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext::QueryInterface</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwnerServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContextOwnerServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextOwnerServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60214fdb-212c-4967-8cbf-e988db893245">CreateRange</a>
</td>
<td align="left" width="63%">
Creates a new range based upon a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f77d82f-e048-463f-bf0d-15bf1daaddb6">ForceLoadProperty</a>
</td>
<td align="left" width="63%">
Forces a property load.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aae92e2-ae08-4e87-88f1-ece448323866">OnAttributeChange</a>
</td>
<td align="left" width="63%">
Called by a context owner to generate notifications that a support attribute value changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9e17687-6be6-4d2d-ba3a-6c128e71de26">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Called by the context owner when the on-screen representation of the text stream is updated during a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da450910-d592-49c0-8df7-bc2f4037c4d2">OnStatusChange</a>
</td>
<td align="left" width="63%">
Called by the context owner when the dwDynamicFlags member of the TS_STATUS structure returned by the ITfContextOwner::GetStatus method changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e67b6fa7-610d-426f-a290-36c0da4068f4">Serialize</a>
</td>
<td align="left" width="63%">
Obtains a property from a range of text and writes the property data into a stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b02ffedf-83c5-48ff-8116-801aaec6dc71">Unserialize</a>
</td>
<td align="left" width="63%">
Applies previously serialized property data to a property object.

</td>
</tr>
</table> 

