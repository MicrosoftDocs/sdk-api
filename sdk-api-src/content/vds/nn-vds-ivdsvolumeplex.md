---
UID: NN:vds.IVdsVolumePlex
title: IVdsVolumePlex (vds.h)
author: windows-sdk-content
description: Provides methods for maintaining volume plexes.
old-location: base\ivdsvolumeplex.htm
tech.root: VDS
ms.assetid: 91970f8b-2b19-4054-8aa2-28e1ea74b3f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsVolumePlex, IVdsVolumePlex interface [VDS], IVdsVolumePlex interface [VDS],described, base.ivdsvolumeplex, vds/IVdsVolumePlex
ms.topic: interface
f1_keywords: ["vds/IVdsVolumePlex"]
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
 - IVdsVolumePlex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVolumePlex interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for maintaining volume plexes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVolumePlex</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVolumePlex</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property information of the current volume plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-getvolume">GetVolume</a>
</td>
<td align="left" width="63%">
Returns the volume to which the current plex is a member.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-queryextents">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns all extents for the current plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-repair">Repair</a>
</td>
<td align="left" width="63%">
Repairs a fault-tolerant volume plex by moving bad members to good disks.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-queryplexes">IVdsVolume::QueryPlexes</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_volume_plex_prop">VDS_VOLUME_PLEX_PROP</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/volume-plex-object">Volume Plex Object</a>
 

 

