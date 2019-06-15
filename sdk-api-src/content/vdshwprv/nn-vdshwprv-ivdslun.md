---
UID: NN:vdshwprv.IVdsLun
title: IVdsLun (vdshwprv.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on a logical unit number (LUN).
old-location: base\ivdslun.htm
tech.root: VDS
ms.assetid: e2fbebc0-593e-437c-a401-80e35a43da94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsLun, IVdsLun interface [VDS], IVdsLun interface [VDS],described, base.ivdslun, vds/IVdsLun, vdshwprv/IVdsLun
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
 - IVdsLun
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsLun interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a logical unit number (LUN).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLun</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLun</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-addplex">AddPlex</a>
</td>
<td align="left" width="63%">
Adds a LUN to the target LUN as a new plex.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-applyhints">ApplyHints</a>
</td>
<td align="left" width="63%">
Applies a new set of hints to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">AssociateControllers</a>
</td>
<td align="left" width="63%">
Sets the subsystem controllers to active or inactive with respect to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the LUN and all of its plexes.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-extend">Extend</a>
</td>
<td align="left" width="63%">
Extends a LUN by a specified number of bytes. The caller can specify a list of drives for the provider to 
     use for extending the LUN, or direct the provider to select the drives automatically.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getidentificationdata">GetIdentificationData</a>
</td>
<td align="left" width="63%">
Returns the LUN identification data, which comprises fields from the SCSI Inquiry Data and Vital Product 
     Data pages 0x80 and 0x83.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the LUN properties.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-getsubsystem">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem that surfaces the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryactivecontrollers">QueryActiveControllers</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the currently active controllers—the 
     controllers through which the LUN is accessible.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">QueryHints</a>
</td>
<td align="left" width="63%">
Returns the hints currently applied to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-querymaxlunextendsize">QueryMaxLunExtendSize</a>
</td>
<td align="left" width="63%">
Returns the maximum size by which a LUN can be extended.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryplexes">QueryPlexes</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUN plexes. All LUNs have at least one plex.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-recover">Recover</a>
</td>
<td align="left" width="63%">
Starts a recovery operation on a LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-removeplex">RemovePlex</a>
</td>
<td align="left" width="63%">
Removes a plex from a LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-setmask">SetMask</a>
</td>
<td align="left" width="63%">
Specifies the LUN unmasking list—the list of computers on the network to be granted 
    access to the LUN.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the LUN status to the specified value.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-shrink">Shrink</a>
</td>
<td align="left" width="63%">
Shrinks a LUN by a specified number of bytes.</p> (Inherited from <b>IVdsLun</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-getlun">IVdsLunPlex::GetLun</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/lun-object">LUN Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

