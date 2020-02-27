---
UID: NN:vdshwprv.IVdsControllerPort
title: IVdsControllerPort (vdshwprv.h)
description: Provides methods for performing query and configuration operations on a controller port.
old-location: base\ivdscontrollerport.htm
tech.root: VDS
ms.assetid: a0ceaf1d-b839-4cf7-b64e-9100f3cf23ef
ms.date: 12/05/2018
ms.keywords: IVdsControllerPort, IVdsControllerPort interface [VDS], IVdsControllerPort interface [VDS],described, base.ivdscontrollerport, vds/IVdsControllerPort, vdshwprv/IVdsControllerPort
f1_keywords:
- vdshwprv/IVdsControllerPort
dev_langs:
- c++
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
- IVdsControllerPort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsControllerPort interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing 
   query and configuration operations on a controller port.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsControllerPort</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsControllerPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsControllerPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-getcontroller">GetController</a>
</td>
<td align="left" width="63%">
Returns the controller to which the controller port belongs.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of a controller port.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-queryassociatedluns">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs with which the controller port is associated—the LUNs 
     for which the controller is active. This method replaces 
     <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-queryassociatedluns">IVdsController::QueryAssociatedLuns</a>.
 (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-reset">Reset</a>
</td>
<td align="left" width="63%">
Reinitializes the controller port.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollerport-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of a controller port to the specified value.</p> (Inherited from <b>IVdsControllerPort</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

