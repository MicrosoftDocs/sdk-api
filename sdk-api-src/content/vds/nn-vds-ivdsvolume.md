---
UID: NN:vds.IVdsVolume
title: IVdsVolume (vds.h)
author: windows-sdk-content
description: Provides methods to manage volumes.
old-location: base\ivdsvolume.htm
tech.root: VDS
ms.assetid: a02ee0a6-ac29-406c-9fc0-4f632d32424f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolume, IVdsVolume interface [VDS], IVdsVolume interface [VDS],described, base.ivdsvolume, vds/IVdsVolume
ms.topic: interface
f1_keywords: 
 - "vds/IVdsVolume"
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
 - IVdsVolume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolume interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to manage volumes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolume</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolume</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-addplex">AddPlex</a>
</td>
<td align="left" width="63%">
Adds a volume as a plex to the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-breakplex">BreakPlex</a>
</td>
<td align="left" width="63%">
Removes a specified plex from the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-clearflags">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the volumes flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes all plexes in the current volume, releasing the extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">Extend</a>
</td>
<td align="left" width="63%">
Expands the size of the current volume by adding disk extents to the members of each plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-getpack">GetPack</a>
</td>
<td align="left" width="63%">
Returns the pack to which the volume is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property information of the current volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-queryplexes">QueryPlexes</a>
</td>
<td align="left" width="63%">
Returns an enumeration that contains all plexes for the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-removeplex">RemovePlex</a>
</td>
<td align="left" width="63%">
Removes one or more specified plexes from the current volume, releasing the extents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the volume flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-shrink">Shrink</a>
</td>
<td align="left" width="63%">
Reduces the size of all volume plexes and releases the extents.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-queryvolumes">IVdsPack::QueryVolumes</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_volume_prop">VDS_VOLUME_PROP</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/volume-object">Volume Object</a>
 

 

