---
UID: NN:mswmdm.IWMDMStorage4
title: IWMDMStorage4
author: windows-sdk-content
description: The IWMDMStorage4 interface extends IWMDMStorage3 by providing methods for retrieving a subset of available metadata for a storage, and for setting and retrieving a list of references to other storages.
old-location: wmdm\iwmdmstorage4.htm
tech.root: WMDM
ms.assetid: ac80cc08-0ff0-48ee-b9c6-e094f803b751
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMDMStorage4, IWMDMStorage4 interface [windows Media Device Manager], IWMDMStorage4 interface [windows Media Device Manager],described, IWMDMStorage4Interface, mswmdm/IWMDMStorage4, wmdm.iwmdmstorage4
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
 - IWMDMStorage4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorage4 interface


## -description



The <b>IWMDMStorage4</b> interface extends <b>IWMDMStorage3</b> by providing methods for retrieving a subset of available metadata for a storage, and for setting and retrieving a list of references to other storages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage4</b> interface inherits from <a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3</a>. <b>IWMDMStorage4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93ca4488-beaf-4617-99ba-19bb7707d4ba">FindStorage</a>
</td>
<td align="left" width="63%">
Retrieves a storage in the current root storage by its unique identification (ID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3281501-ec4b-4437-b462-d5b0fd1ac4e0">GetParent</a>
</td>
<td align="left" width="63%">
Retrieves the parent of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8199de99-3660-4819-a8e0-ae8e3aa1680e">GetReferences</a>
</td>
<td align="left" width="63%">
Retrieves an array of pointers to <b>IWMDMStorage</b> pointed to by this storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63df4448-75f0-4152-a308-15f6f10e8564">GetRightsWithProgress</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4e2c889-9ad0-42d1-bb50-4ebcb9859715">GetSpecifiedMetadata</a>
</td>
<td align="left" width="63%">
Retrieves one or more specific metadata properties from the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f61b8c4e-6ea1-49a3-8b61-c3ea8bfe2714">SetReferences</a>
</td>
<td align="left" width="63%">
Sets the references contained in a storage that has references (such as a playlist or album), overwriting any previously existing references held by the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2 Interface</a>



<a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

