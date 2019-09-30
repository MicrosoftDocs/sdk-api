---
UID: NN:vds.IVdsService
title: IVdsService (vds.h)
author: windows-sdk-content
description: Provides methods to query and interact with VDS.
old-location: base\ivdsservice.htm
tech.root: VDS
ms.assetid: 6b081cc8-fe06-427f-b06d-831a1f1fef52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsService, IVdsService interface [VDS], IVdsService interface [VDS],described, base.ivdsservice, vds/IVdsService
ms.topic: interface
f1_keywords:
- vds/IVdsService
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
- IVdsService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsService interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and interact with VDS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-advise">Advise</a>
</td>
<td align="left" width="63%">
Registers the caller's <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface with VDS so that the caller receives notifications from the VDS service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-cleanupobsoletemountpoints">CleanupObsoleteMountPoints</a>
</td>
<td align="left" width="63%">
Updates the registry by removing user-mode paths and mounted folders for volumes that no longer exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-clearflags">ClearFlags</a>
</td>
<td align="left" width="63%">
Clears the service object flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Returns an object pointer for the identified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves VDS property information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-isserviceready">IsServiceReady</a>
</td>
<td align="left" width="63%">
Indicates the status of VDS initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-querydriveletters">QueryDriveLetters</a>
</td>
<td align="left" width="63%">
Returns the property information of one or more drive letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryfilesystemtypes">QueryFileSystemTypes</a>
</td>
<td align="left" width="63%">
Returns the property information of all the file systems known to VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-querymaskeddisks">QueryMaskedDisks</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">QueryProviders</a>
</td>
<td align="left" width="63%">
Enumerates all the hardware or software providers known to VDS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-queryunallocateddisks">QueryUnallocatedDisks</a>
</td>
<td align="left" width="63%">
Enumerates  all the unallocated disks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-reboot">Reboot</a>
</td>
<td align="left" width="63%">
Restarts the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-reenumerate">Reenumerate</a>
</td>
<td align="left" width="63%">
Discovers new disks, removed disks, or both.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes disk ownership and layout.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the service object flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters the caller's  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface so that the caller no longer receives notifications from the VDS service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsservice-waitforserviceready">WaitForServiceReady</a>
</td>
<td align="left" width="63%">
Waits until initialization either completes successfully (or fails) before invoking methods exposed by VDS objects.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/startup-and-service-objects">Startup and Service Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a>
 

 

