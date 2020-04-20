---
UID: NN:vds.IVdsMaintenance
title: IVdsMaintenance (vds.h)
description: Provides methods for performing maintenance operations on a subsystem, controller, LUN, or drive.helpviewer_keywords: ["IVdsMaintenance","IVdsMaintenance interface [VDS]","IVdsMaintenance interface [VDS]","described","base.ivdsmaintenance","vds/IVdsMaintenance","vdshwprv/IVdsMaintenance"]
old-location: base\ivdsmaintenance.htm
tech.root: VDS
ms.assetid: 08c01459-151a-4dd8-bea5-412076e39a8a
ms.date: 12/05/2018
ms.keywords: IVdsMaintenance, IVdsMaintenance interface [VDS], IVdsMaintenance interface [VDS],described, base.ivdsmaintenance, vds/IVdsMaintenance, vdshwprv/IVdsMaintenance
f1_keywords:
- vds/IVdsMaintenance
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
- IVdsMaintenance
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsMaintenance interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods for performing maintenance operations on a subsystem, controller, LUN, or drive.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsMaintenance</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsMaintenance</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsMaintenance</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">PulseMaintenance</a>
</td>
<td align="left" width="63%">
Performs the specified operation a specified number of times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-startmaintenance">StartMaintenance</a>
</td>
<td align="left" width="63%">
Starts a maintenance operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">StopMaintenance</a>
</td>
<td align="left" width="63%">
Stops a maintenance operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

