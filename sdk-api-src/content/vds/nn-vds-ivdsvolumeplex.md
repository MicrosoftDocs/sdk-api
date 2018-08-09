---
UID: NN:vds.IVdsVolumePlex
title: IVdsVolumePlex
author: windows-sdk-content
description: Provides methods for maintaining volume plexes.
old-location: base\ivdsvolumeplex.htm
old-project: vds
ms.assetid: 91970f8b-2b19-4054-8aa2-28e1ea74b3f6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsVolumePlex, IVdsVolumePlex interface [VDS], IVdsVolumePlex interface [VDS],described, base.ivdsvolumeplex, vds/IVdsVolumePlex
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumePlex
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumePlex interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for maintaining volume plexes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumePlex</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVolumePlex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVolumePlex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property information of the current volume plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddf6102b-81d4-4604-942e-ffb1c2c4730f">GetVolume</a>
</td>
<td align="left" width="63%">
Returns the volume to which the current plex is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09548bcc-29b9-498f-a4c0-99428f26343a">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns all extents for the current plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21c91e85-8a49-4e74-9191-37aeb03b299e">Repair</a>
</td>
<td align="left" width="63%">
Repairs a fault-tolerant volume plex by moving bad members to good disks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33fc5b7c-4d05-4ec7-8d03-631c6d9f2f34">IVdsVolume::QueryPlexes</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/9e770bfc-2bcb-45f0-a7fc-ba526349839e">Volume Plex Object</a>
 

 

