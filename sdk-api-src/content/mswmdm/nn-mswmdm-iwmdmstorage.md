---
UID: NN:mswmdm.IWMDMStorage
title: IWMDMStorage
author: windows-sdk-content
description: An instance of the IWMDMStorage interface provides methods to examine and explore a storage (a generic name for a data or collection object, such as a file, folder, or playlist) on a device.
old-location: wmdm\iwmdmstorage.htm
tech.root: WMDM
ms.assetid: 1ede7c68-0169-4375-9b45-b0995ad14e44
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMDMStorage, IWMDMStorage interface [windows Media Device Manager], IWMDMStorage interface [windows Media Device Manager],described, IWMDMStorageInterface, mswmdm/IWMDMStorage, wmdm.iwmdmstorage
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
 - IWMDMStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorage interface


## -description



An instance of the <b>IWMDMStorage</b> interface provides methods to examine and explore a storage (a generic name for a data or collection object, such as a file, folder, or playlist) on a <i>device</i>. Note that storages cannot be used to refer to objects on the computer, only on the device. <b>IWMDMStorage</b> can contain nested objects, and can represent the root object (the entire storage medium) or any child object, such as a folder or file, on that medium. The <b>IWMDMStorage2</b> interface extends this interface by making it possible to get a storage pointer from a storage name and to get and set extended attributes. <b>IWMDMStorage3</b> extends this interface by supporting metadata.

To obtain a root storage object which can be queried for all other objects on a device, you must call <a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">IWMDMDevice::EnumStorage</a>, as described in <a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IWMDMEnumStorage</b> interface to enumerate the immediate child storages of the current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e43139d2-260a-4f27-a06c-aca741204663">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53693e2f-f6d2-42cc-9387-798f8dc10556">GetDate</a>
</td>
<td align="left" width="63%">
Retrieves the date on which the storage was most recently modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1387a82f-e320-402a-b3c9-2f28550c4caf">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b654d32-b72a-44cf-a8d9-63fc0ae76171">GetRights</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for a licensed storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1042b71b-1656-4f0b-be95-8a09ba4421ed">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the storage, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0203f881-f838-412b-a796-42f946513c65">GetStorageGlobals</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IWMDMStorageGlobals</b> interface to provide access to global information about a storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e570ad-63d3-4c8f-8569-63aa3645f866">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a command to the storage through Windows Media Device Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">SetAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of the storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2 Interface</a>



<a href="https://msdn.microsoft.com/b62ea18b-c692-464f-a009-727a2924f8b8">IWMDMStorage3 Interface</a>



<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>



<a href="https://msdn.microsoft.com/fe164271-58f0-4b28-a200-6b15f8b42d36">IWMDMStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

