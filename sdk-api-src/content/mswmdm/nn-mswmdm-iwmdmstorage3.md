---
UID: NN:mswmdm.IWMDMStorage3
title: IWMDMStorage3
author: windows-sdk-content
description: The IWMDMStorage3 interface extends IWMDMStorage2 by exposing metadata.
old-location: wmdm\iwmdmstorage3.htm
old-project: WMDM
ms.assetid: b62ea18b-c692-464f-a009-727a2924f8b8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMStorage3, IWMDMStorage3 interface [windows Media Device Manager], IWMDMStorage3 interface [windows Media Device Manager],described, IWMDMStorage3Interface, mswmdm/IWMDMStorage3, wmdm.iwmdmstorage3
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMStorage3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage3 interface


## -description



The <b>IWMDMStorage3</b> interface extends <a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2</a> by exposing metadata.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage3</b> interface inherits from <a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2</a>. <b>IWMDMStorage3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e46b5f30-3dd9-4e5a-bd75-c7716a1d8a2a">CreateEmptyMetadataObject</a>
</td>
<td align="left" width="63%">
Creates an object that supports the <b>IWMDMMetaData</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e436742-fb19-4e8e-98a2-d961c9f0ecbf">GetMetadata</a>
</td>
<td align="left" width="63%">
Retrieves the metadata associated with the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74916098-07d2-4dc9-932d-b174a10032dd">SetEnumPreference</a>
</td>
<td align="left" width="63%">
Sets the preferred enumeration mode for the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f06eb965-af34-4247-b8a6-0ac1ee4e4839">SetMetadata</a>
</td>
<td align="left" width="63%">
Sets metadata on the storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

