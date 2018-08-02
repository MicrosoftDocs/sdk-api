---
UID: NN:vdshwprv.IVdsLun
title: IVdsLun
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a logical unit number (LUN).
old-location: base\ivdslun.htm
old-project: VDS
ms.assetid: e2fbebc0-593e-437c-a401-80e35a43da94
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsLun, IVdsLun interface [VDS], IVdsLun interface [VDS],described, base.ivdslun, vds/IVdsLun, vdshwprv/IVdsLun
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vdshwprv.h
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
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLun
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLun interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a logical unit number (LUN).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLun</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLun</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLun</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d6d746-e740-40b0-b9e1-0c5537d00338">AddPlex</a>
</td>
<td align="left" width="63%">
Adds a LUN to the target LUN as a new plex.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2582913a-bc13-45dc-b0c8-9429945014da">ApplyHints</a>
</td>
<td align="left" width="63%">
Applies a new set of hints to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c3dc668-1745-49f4-9cd1-3bf0b322d0b2">AssociateControllers</a>
</td>
<td align="left" width="63%">
Sets the subsystem controllers to active or inactive with respect to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21522c62-0b60-4c70-b2bd-7a33aa94d280">Delete</a>
</td>
<td align="left" width="63%">
Deletes the LUN and all of its plexes.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922720">Extend</a>
</td>
<td align="left" width="63%">
Extends a LUN by a specified number of bytes. The caller can specify a list of drives for the provider to 
     use for extending the LUN, or direct the provider to select the drives automatically.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab72cbe0-d10d-49af-87a0-4da28f79b124">GetIdentificationData</a>
</td>
<td align="left" width="63%">
Returns the LUN identification data, which comprises fields from the SCSI Inquiry Data and Vital Product 
     Data pages 0x80 and 0x83.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the LUN properties.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd7dbe48-ad56-4304-a076-608f697620d8">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem that surfaces the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82561e4a-f2c2-46da-96bb-fbd50d4f7c39">QueryActiveControllers</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the currently active controllers—the 
     controllers through which the LUN is accessible.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">QueryHints</a>
</td>
<td align="left" width="63%">
Returns the hints currently applied to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac30de71-7a2e-4a65-a37b-34a0d01ca645">QueryMaxLunExtendSize</a>
</td>
<td align="left" width="63%">
Returns the maximum size by which a LUN can be extended.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/128708cb-2ad1-45be-8e38-b5fd943d0945">QueryPlexes</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUN plexes. All LUNs have at least one plex.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/406da360-9aa8-42df-8918-da72b22ce3b5">Recover</a>
</td>
<td align="left" width="63%">
Starts a recovery operation on a LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9959c2a3-f282-4512-9d3f-da8842d5ee79">RemovePlex</a>
</td>
<td align="left" width="63%">
Removes a plex from a LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7e841cc-95b4-452f-ac14-d7063fe6a694">SetMask</a>
</td>
<td align="left" width="63%">
Specifies the LUN unmasking list—the list of computers on the network to be granted 
    access to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a293f129-5238-405a-ba56-bf53ac4ab1d8">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the LUN status to the specified value.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a02f7741-c17a-48f3-a823-292613aa287b">Shrink</a>
</td>
<td align="left" width="63%">
Shrinks a LUN by a specified number of bytes.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/74f9fed5-f33d-4e88-b3d2-7eb8ef33711e">IVdsLunPlex::GetLun</a>



<a href="https://msdn.microsoft.com/ea22bd6d-4a7a-4674-82e9-08460914ff8e">LUN Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

