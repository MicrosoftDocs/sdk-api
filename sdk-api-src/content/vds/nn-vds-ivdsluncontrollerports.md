---
UID: NN:vds.IVdsLunControllerPorts
title: IVdsLunControllerPorts (vds.h)
description: Provides methods for performing controller port configuration operations on a LUN.
helpviewer_keywords: ["IVdsLunControllerPorts","IVdsLunControllerPorts interface [VDS]","IVdsLunControllerPorts interface [VDS]","described","base.ivdsluncontrollerports","vds/IVdsLunControllerPorts","vdshwprv/IVdsLunControllerPorts"]
old-location: base\ivdsluncontrollerports.htm
tech.root: base
ms.assetid: 81e48874-8bc2-4b82-bcf8-ce87f99ca3ad
ms.date: 12/05/2018
ms.keywords: IVdsLunControllerPorts, IVdsLunControllerPorts interface [VDS], IVdsLunControllerPorts interface [VDS],described, base.ivdsluncontrollerports, vds/IVdsLunControllerPorts, vdshwprv/IVdsLunControllerPorts
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsLunControllerPorts
 - vds/IVdsLunControllerPorts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLunControllerPorts
---

# IVdsLunControllerPorts interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides 
   methods for performing controller port configuration operations on a LUN.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunControllerPorts</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsLunControllerPorts</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunControllerPorts</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluncontrollerports-associatecontrollerports">AssociateControllerPorts</a>
</td>
<td align="left" width="63%">
Sets the subsystem controller ports to active or inactive with respect to the LUN. This method replaces 
     <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-associatecontrollers">IVdsLun::AssociateControllers</a>.
 (Inherited from <b>IVdsLunControllerPorts</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluncontrollerports-queryactivecontrollerports">QueryActiveControllerPorts</a>
</td>
<td align="left" width="63%">
Returns an enumeration of currently active controller ports.</p> (Inherited from <b>IVdsLunControllerPorts</b>)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>