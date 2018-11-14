---
UID: NN:vds.IVdsLunPlex
title: IVdsLunPlex
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a LUN plex.
old-location: base\ivdslunplex.htm
tech.root: VDS
ms.assetid: de795ae2-784c-43d7-a34c-546af31d2747
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsLunPlex, IVdsLunPlex interface [VDS], IVdsLunPlex interface [VDS],described, base.ivdslunplex, vds/IVdsLunPlex, vdshwprv/IVdsLunPlex
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
 - IVdsLunPlex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsLunPlex interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a LUN plex.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunPlex</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLunPlex</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunPlex</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66299644-4b70-4cd3-ae99-4d4084c3c3c5">ApplyHints</a>
</td>
<td align="left" width="63%">
Applies a new set of hints to the LUN plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74f9fed5-f33d-4e88-b3d2-7eb8ef33711e">GetLun</a>
</td>
<td align="left" width="63%">
Returns the LUN object to which the plex object belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ded24edd-fa6a-48f3-a448-690078f034bb">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the LUN plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ed5bdd-c696-47cc-84c8-266b230f7970">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns an array of the drive extents that contribute to the plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ecb0840-8eaf-47c9-b8a9-98c738ed7daf">QueryHints</a>
</td>
<td align="left" width="63%">
Returns the hints that are currently applied to the LUN plex.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db6eabaa-1b84-4613-ab2a-8d5904305e08">LUN Plex Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

