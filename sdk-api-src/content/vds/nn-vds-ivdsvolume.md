---
UID: NN:vds.IVdsVolume
title: IVdsVolume
author: windows-sdk-content
description: Provides methods to manage volumes.
old-location: base\ivdsvolume.htm
old-project: VDS
ms.assetid: a02ee0a6-ac29-406c-9fc0-4f632d32424f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsVolume, IVdsVolume interface [VDS], IVdsVolume interface [VDS],described, base.ivdsvolume, vds/IVdsVolume
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsVolume
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolume interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to manage volumes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolume</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolume</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolume</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b463ad74-400d-4100-83ff-3eb98e6a0db4">AddPlex</a>
</td>
<td align="left" width="63%">
Adds a volume as a plex to the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7e42aa4-3233-40e9-b537-043eecd192ad">BreakPlex</a>
</td>
<td align="left" width="63%">
Removes a specified plex from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/970dcd4a-ac06-4e2d-969c-82c5dabd0019">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the volumes flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cc7cb6d-4495-41b7-8fe5-d2e1f574ed70">Delete</a>
</td>
<td align="left" width="63%">
Deletes all plexes in the current volume, releasing the extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922720">Extend</a>
</td>
<td align="left" width="63%">
Expands the size of the current volume by adding disk extents to the members of each plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8719c4a4-a7d6-4329-a601-5c88de18f53d">GetPack</a>
</td>
<td align="left" width="63%">
Returns the pack to which the volume is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property information of the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33fc5b7c-4d05-4ec7-8d03-631c6d9f2f34">QueryPlexes</a>
</td>
<td align="left" width="63%">
Returns an enumeration that contains all plexes for the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724f80e7-4656-4956-aaad-9f778329f139">RemovePlex</a>
</td>
<td align="left" width="63%">
Removes one or more specified plexes from the current volume, releasing the extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the volume flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63ac6ef9-0e84-40ed-a302-4f32316a41cc">Shrink</a>
</td>
<td align="left" width="63%">
Reduces the size of all volume plexes and releases the extents.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/43f9972d-14a6-4674-bf90-741ad3a9eb0d">IVdsPack::QueryVolumes</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/92013015-b0f5-4b92-937b-c2637f65810c">Volume Object</a>
 

 

