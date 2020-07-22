---
UID: NN:vds.IVdsControllerControllerPort
title: IVdsControllerControllerPort (vds.h)
description: Provides a method to enumerate controller ports for a class implementing the IVdsController interface. This is needed to support MPIO.
helpviewer_keywords: ["IVdsControllerControllerPort","IVdsControllerControllerPort interface [VDS]","IVdsControllerControllerPort interface [VDS]","described","base.ivdscontrollercontrollerport","vds/IVdsControllerControllerPort","vdshwprv/IVdsControllerControllerPort"]
old-location: base\ivdscontrollercontrollerport.htm
tech.root: base
ms.assetid: 15b09f97-c729-4687-a62c-dac57661f8c0
ms.date: 12/05/2018
ms.keywords: IVdsControllerControllerPort, IVdsControllerControllerPort interface [VDS], IVdsControllerControllerPort interface [VDS],described, base.ivdscontrollercontrollerport, vds/IVdsControllerControllerPort, vdshwprv/IVdsControllerControllerPort
f1_keywords:
- vds/IVdsControllerControllerPort
dev_langs:
- c++
req.header: vds.h
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
- IVdsControllerControllerPort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsControllerControllerPort interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides a method to enumerate controller ports for a class implementing the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a> interface. This is needed to support 
   MPIO.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsControllerControllerPort</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsControllerControllerPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsControllerControllerPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollercontrollerport-querycontrollerports">QueryControllerPorts</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> object that enumerates the 
     ports of the controller.</p> (Inherited from <b>IVdsControllerControllerPort</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/controller-object">Controller Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontrollercontrollerport-querycontrollerports">QueryControllerPorts</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

