---
UID: NN:mswmdm.IWMDMStorage2
title: IWMDMStorage2 (mswmdm.h)
author: windows-sdk-content
description: The IWMDMStorage2 interface extends IWMDMStorage by making it possible to get a child storage by name, and to get and set extended attributes. IWMDMStorage3 interface extends this interface by supporting metadata.
old-location: wmdm\iwmdmstorage2.htm
tech.root: WMDM
ms.assetid: 1283a5b5-d893-4795-a50a-5a3bd6fce8d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMStorage2, IWMDMStorage2 interface [windows Media Device Manager], IWMDMStorage2 interface [windows Media Device Manager],described, IWMDMStorage2Interface, mswmdm/IWMDMStorage2, wmdm.iwmdmstorage2
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
 - IWMDMStorage2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorage2 interface


## -description



The <b>IWMDMStorage2</b> interface extends <b>IWMDMStorage</b> by making it possible to get a child storage by name, and to get and set extended attributes. <b>IWMDMStorage3</b> interface extends this interface by supporting metadata.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage2</b> interface inherits from <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a>. <b>IWMDMStorage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8212ab78-0a2a-41cd-8a7c-da6e3886b586">GetAttributes2</a>
</td>
<td align="left" width="63%">
Retrieves extended attributes of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be7b3da1-583b-4bad-8e35-19f309242744">GetStorage</a>
</td>
<td align="left" width="63%">
Retrieves a child storage by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a2e143e-8d6a-497e-9c45-fd3349c4ec97">SetAttributes2</a>
</td>
<td align="left" width="63%">
Sets extended attributes of the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3 Interface</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

