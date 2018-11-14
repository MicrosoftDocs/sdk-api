---
UID: NN:mswmdm.IWMDMMetaData
title: IWMDMMetaData
author: windows-sdk-content
description: The IWMDMMetaData interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage.
old-location: wmdm\iwmdmmetadata.htm
tech.root: WMDM
ms.assetid: ea57a851-0b9f-444c-9819-a278f2ece2b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMMetaData, IWMDMMetaData interface [windows Media Device Manager], IWMDMMetaData interface [windows Media Device Manager],described, IWMDMMetaDataInterface, mswmdm/IWMDMMetaData, wmdm.iwmdmmetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - mswmdm.h
api_name:
 - IWMDMMetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMMetaData interface


## -description



The <b>IWMDMMetaData</b> interface sets and retrieves metadata properties (such as artist, album, genre, and so on) of a storage. Metadata properties are stored as name-value pairs.

To create a new, empty instance of this interface, call <a href="https://msdn.microsoft.com/e46b5f30-3dd9-4e5a-bd75-c7716a1d8a2a">IWMDMStorage3::CreateEmptyMetadataObject</a>. To retrieve this interface (with values), call <a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">IWMDMStorage3::GetMetadata</a> or <a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">IWMDMStorage4::GetSpecifiedMetadata</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMMetaData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMMetaData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMMetaData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb8dee5f-034f-4e1d-86fe-34a2d9439e5f">AddItem</a>
</td>
<td align="left" width="63%">
Adds a metadata property to the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f7f9661-d632-4502-940b-6d83fc32cdad">GetItemCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of properties held by the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d27e1e9-ab91-433d-8216-ace195386d44">QueryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e793954b-6aef-4088-97cb-eb1f050cc64b">QueryByName</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property specified by name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>



<a href="https://msdn.microsoft.com/870c0e36-aa26-4ab3-b47f-81346d005fa5">Metadata Constants</a>



<a href="https://msdn.microsoft.com/478a5412-e8b4-41c8-802f-9c2748dbaeae">Setting Metadata on a File</a>
 

 

