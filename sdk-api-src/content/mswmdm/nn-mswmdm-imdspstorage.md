---
UID: NN:mswmdm.IMDSPStorage
title: IMDSPStorage (mswmdm.h)
author: windows-sdk-content
description: The IMDSPStorage interface provides an instanced-based association with a storage medium on a device.
old-location: wmdm\imdspstorage.htm
tech.root: WMDM
ms.assetid: f22b8a6d-7df8-4fea-9436-79b9ded25a40
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPStorage, IMDSPStorage interface [windows Media Device Manager], IMDSPStorage interface [windows Media Device Manager],described, IMDSPStorageInterface, mswmdm/IMDSPStorage, wmdm.imdspstorage
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
 - IMDSPStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage interface


## -description



The <b>IMDSPStorage</b> interface provides an instanced-based association with a storage medium on a device. An <b>IMDSPStorage</b> interface can represent the entire storage medium, or can be further enumerated to represent any object, such as a folder or file, on that medium. This reiterative enumeration provides the mechanism for describing the organization of a hierarchically structured storage medium.

The methods of <b>IMDSPStorage</b> can be used to gather information about the object that the interface represents. The <a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2</a> interface extends <b>IMDSPStorage</b> by getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95633bc4-44fc-4ac7-9492-f99069d77d4d">CreateStorage</a>
</td>
<td align="left" width="63%">
Creates a new storage and returns a pointer to the <b>IMDSPStorage</b> interface on the newly created storage. The new storage can be created at the same level or can be inserted into the current storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b97d023-172f-4335-8d15-e5a4b67f24b8">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves the attributes of the storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/822a5a3f-e649-4e5c-8216-56e77d60a8e3">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the date on which the storage object (file or folder) was most recently modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ba0c598-9ea2-42cc-a234-1c0e192971a8">GetDate</a>
</td>
<td align="left" width="63%">
Accesses the <b>IMDSPEnumStorage</b> interface to enumerate the individual storage media on a device

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6172f222-8b92-4da5-8001-b79431c26518">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4fb3ace-ebb5-4d95-8fce-780b5dc8e21a">GetRights</a>
</td>
<td align="left" width="63%">
Retrieves the size of the storage object, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95b28f9a-744c-4d49-a91c-6652d688b91a">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IMDSPStorageGlobals</b> interface to provide access to global information about a storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93c963ea-9b00-4897-838c-fdc06c781a2d">GetStorageGlobals</a>
</td>
<td align="left" width="63%">
Retrieves the rights information for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8a43a21-6ea4-4402-b0fc-2ce7868c83d7">SendOpaqueCommands</a>
</td>
<td align="left" width="63%">
Sends commands through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e995b255-364f-4ea6-b7fd-4443e84432ef">SetAttributes</a>
</td>
<td align="left" width="63%">
Sets the attributes of the storage object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fc2fed46-1f4d-4d53-a843-0f699b687a18">IMDSPEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>



<a href="https://msdn.microsoft.com/5ff674a1-a0b9-43b6-b8b7-9a5c67b3f919">IMDSPStorage3 Interface</a>



<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>



<a href="https://msdn.microsoft.com/70653352-a467-4197-93e3-e8fb45f99d34">IMDSPStorageGlobals Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

