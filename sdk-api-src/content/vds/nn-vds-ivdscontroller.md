---
UID: NN:vds.IVdsController
title: IVdsController (vds.h)
description: Provides methods for performing query and configuration operations on a controller.
old-location: base\ivdscontroller.htm
tech.root: VDS
ms.assetid: cc30a78a-78a4-49c2-a97d-228400da46a9
ms.date: 12/05/2018
ms.keywords: IVdsController, IVdsController interface [VDS], IVdsController interface [VDS],described, base.ivdscontroller, vds/IVdsController, vdshwprv/IVdsController
ms.topic: interface
f1_keywords:
- vds/IVdsController
dev_langs:
- c++
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
- IVdsController
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsController interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for 
   performing query and configuration operations on a controller.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsController</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsController</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsController</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-flushcache">FlushCache</a>
</td>
<td align="left" width="63%">
Flushes the cache of the controller to a persistent store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getportproperties">GetPortProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the specified controller port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the controller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-getsubsystem">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the controller belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-invalidatecache">InvalidateCache</a>
</td>
<td align="left" width="63%">
Invalidates the cache of the controller. All data in the cache is lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-queryassociatedluns">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs with which the controller is associated—in other words, the LUNs for which the controller is active.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-reset">Reset</a>
</td>
<td align="left" width="63%">
Reinitializes the controller and invalidates its cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of the controller to the specified value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/controller-object">Controller Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontrollercontrollerport">IVdsControllerControllerPort</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querycontrollers">IVdsSubSystem::QueryControllers</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_controller_prop">VDS_CONTROLLER_PROP</a>
 

 

