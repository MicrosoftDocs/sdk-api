---
UID: NN:vds.IVdsLunPlex
title: IVdsLunPlex (vds.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a LUN plex.
old-location: base\ivdslunplex.htm
tech.root: VDS
ms.assetid: de795ae2-784c-43d7-a34c-546af31d2747
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsLunPlex, IVdsLunPlex interface [VDS], IVdsLunPlex interface [VDS],described, base.ivdslunplex, vds/IVdsLunPlex, vdshwprv/IVdsLunPlex
ms.topic: interface
f1_keywords: 
 - "vds/IVdsLunPlex"
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
ms.custom: 19H1
---

# IVdsLunPlex interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing query and configuration operations on a LUN plex.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunPlex</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunPlex</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-applyhints">ApplyHints</a>
</td>
<td align="left" width="63%">
Applies a new set of hints to the LUN plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-getlun">GetLun</a>
</td>
<td align="left" width="63%">
Returns the LUN object to which the plex object belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the LUN plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">QueryExtents</a>
</td>
<td align="left" width="63%">
Returns an array of the drive extents that contribute to the plex.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryhints">QueryHints</a>
</td>
<td align="left" width="63%">
Returns the hints that are currently applied to the LUN plex.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/lun-plex-object">LUN Plex Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

