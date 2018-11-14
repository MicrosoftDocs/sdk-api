---
UID: NN:vds.IVdsPack
title: IVdsPack
author: windows-sdk-content
description: Provides methods to query and perform management operations on a pack containing disks and volumes.
old-location: base\ivdspack.htm
tech.root: VDS
ms.assetid: 106989fe-d1dd-4c7f-b889-00a671c6e567
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsPack, IVdsPack interface [VDS], IVdsPack interface [VDS],described, base.ivdspack, vds/IVdsPack
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsPack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsPack interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and 
   perform management operations on a pack containing disks and volumes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsPack</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsPack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsPack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e64e3891-74c6-4014-9909-24f75f69e06d">AddDisk</a>
</td>
<td align="left" width="63%">
Adds a disk to an online pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">CreateVolume</a>
</td>
<td align="left" width="63%">
Creates a volume within the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0793642c-1905-470c-a69f-8bf5f8bbe90d">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property details of a pack object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6e7ca7c-b95f-457d-996b-b3c449b6ce6b">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the provider for the current pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7e85c4c-fb7c-48de-abd7-8d65ecb9a1fa">MigrateDisks</a>
</td>
<td align="left" width="63%">
Migrates a set of disks from one pack to another pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/115c1900-5fea-4e39-be3e-b6d04ceb8a58">QueryDisks</a>
</td>
<td align="left" width="63%">
Enumerates the disks in the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43f9972d-14a6-4674-bf90-741ad3a9eb0d">QueryVolumes</a>
</td>
<td align="left" width="63%">
Enumerates the volumes in the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e558c2f4-e1a9-47c0-9b2f-972457e27bbf">Recover</a>
</td>
<td align="left" width="63%">
Returns a failing or failed pack to a healthy state, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7bdd5b9-430b-49c8-8476-be15eb3948c6">RemoveMissingDisk</a>
</td>
<td align="left" width="63%">
Removes a dynamic disk that is missing from the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fc59ed0-ef54-4834-90d3-309d297543e6">ReplaceDisk</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f30494d8-ae82-479d-a47a-7087129e7e6a">IVdsSwProvider::QueryPacks</a>



<a href="https://msdn.microsoft.com/e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9">Pack Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a>
 

 

