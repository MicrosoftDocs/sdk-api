---
UID: NN:mswmdm.IMDSPStorage4
title: IMDSPStorage4
author: windows-sdk-content
description: The IMDSPStorage4 interface extends IMDSPStorage3 for supporting virtual storages (such as playlists and albums) and metadata.Note  Unless the service provider has added the device parameter UseExtendedWmdm with a value of 1, Windows Media Device Manager will not call this interface. See Device Parameters for more information about this. .
old-location: wmdm\imdspstorage4.htm
tech.root: WMDM
ms.assetid: c1236acc-1f11-4501-9374-2486f7d61db3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMDSPStorage4, IMDSPStorage4 interface [windows Media Device Manager], IMDSPStorage4 interface [windows Media Device Manager],described, IMDSPStorage4Interface, mswmdm/IMDSPStorage4, wmdm.imdspstorage4
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
 - IMDSPStorage4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage4 interface


## -description



The <b>IMDSPStorage4</b> interface extends <a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3</a> for supporting virtual storages (such as playlists and albums) and metadata.

<div class="alert"><b>Note</b>  Unless the service provider has added the device parameter <b>UseExtendedWmdm</b> with a value of 1, Windows Media Device Manager will not call this interface. See <a href="https://msdn.microsoft.com/d8774c85-b5c0-4d9e-8a8e-d60ffdf59549">Device Parameters</a> for more information about this.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage4</b> interface inherits from <a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3</a>. <b>IMDSPStorage4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/493eb6f1-fc06-4b37-803f-a81219e9f819">CreateStorageWithMetadata</a>
</td>
<td align="left" width="63%">
Creates a new storage supporting metadata, and returns a pointer to the <b>IMDSPStorage</b> interface on the newly created storage. The new storage can be created at the same level or can be inserted into the current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/024a295a-ab23-4ee8-963b-1c18e244627a">FindStorage</a>
</td>
<td align="left" width="63%">
Retrieves the storage through its unique identification (ID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b8264ef-9288-4196-9b92-a54a25aad795">GetParent</a>
</td>
<td align="left" width="63%">
Retrieves the parent storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8caf10b-69d4-4d37-836e-af260840254f">GetReferences</a>
</td>
<td align="left" width="63%">
Retrieves references of an association object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f7b3a68-97b3-4470-8ca8-e8eb8a5f83b7">GetSpecifiedMetadata</a>
</td>
<td align="left" width="63%">
Retrieves the specified metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45fd9efa-b03d-46de-9d8c-85ed04d446dd">SetReferences</a>
</td>
<td align="left" width="63%">
Sets references of an association object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>



<a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

