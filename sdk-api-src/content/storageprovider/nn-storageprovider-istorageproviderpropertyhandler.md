---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IStorageProviderPropertyHandler interface


## -description


Provides a collection of properties associated with a file or folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStorageProviderPropertyHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStorageProviderPropertyHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStorageProviderPropertyHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C1E21E6E-A651-4AB3-A4C1-ADDF874DCCC7">RetrieveProperties</a>
</td>
<td align="left" width="63%">
Gets the properties managed by the sync engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/983751BA-BF36-4018-A95A-4BEA1E9BA3BF">SaveProperties</a>
</td>
<td align="left" width="63%">
Saves properties associated with a file or folder.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Caution</b>  <p class="note">You should only implement this interface if you have a specific need to do so.  

</div>
<div> </div>
This interface can be implemented by a cloud storage provider sync engine to share properties about a file or file folder. An instance of <b>IStorageProviderPropertyHandler</b> exists for the lifetime of a storage file created under a sync root. Use <a href="https://msdn.microsoft.com/96DEA181-8506-4FCC-85E0-A2EF79BA6C6D">IStorageProviderHandler</a> to retrieve the set of properties associated with an individual file or folder.

This interface is responsible for keeping track of the following properties:

<ul>
<li>StorageProviderFileIdentifier</li>
<li>StorageProviderFileRemoteUri</li>
<li>StorageProviderFileChecksum</li>
<li>StorageProviderFileVersionWaterline</li>
</ul>


