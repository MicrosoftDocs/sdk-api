---
UID: NN:vds.IEnumVdsObject
title: IEnumVdsObject
author: windows-sdk-content
description: Enumerates through a set of VDS objects of a given type. Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.
old-location: base\ienumvdsobject.htm
old-project: VDS
ms.assetid: 08379071-b3cc-495a-bc8e-ad6cfacd432c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnumVdsObject, IEnumVdsObject interface [VDS], IEnumVdsObject interface [VDS],described, base.ienumvdsobject, vds/IEnumVdsObject, vdshwprv/IEnumVdsObject
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
 - IEnumVdsObject
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IEnumVdsObject interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Enumerates through a 
   set of VDS objects of a given type. Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, 
   disk packs, disks, volumes, or volume plexes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumVdsObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumVdsObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumVdsObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates an enumeration with the same state as the current enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Returns the next object in the enumeration, beginning from the current point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects in the enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0f809c71-a3bd-4c62-8086-9651ea1a3400">Helper Objects</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>
 

 

