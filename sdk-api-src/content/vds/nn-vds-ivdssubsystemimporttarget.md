---
UID: NN:vds.IVdsSubSystemImportTarget
title: IVdsSubSystemImportTarget (vds.h)
description: Provides methods to query and configure the default VSS import target for the subsystem.
helpviewer_keywords: ["IVdsSubSystemImportTarget","IVdsSubSystemImportTarget interface [VDS]","IVdsSubSystemImportTarget interface [VDS]","described","base.ivdssubsystemimporttarget","vds/IVdsSubSystemImportTarget"]
old-location: base\ivdssubsystemimporttarget.htm
tech.root: base
ms.assetid: c9e2f353-d5d4-47a2-8398-5cbd9d499fb7
ms.date: 12/05/2018
ms.keywords: IVdsSubSystemImportTarget, IVdsSubSystemImportTarget interface [VDS], IVdsSubSystemImportTarget interface [VDS],described, base.ivdssubsystemimporttarget, vds/IVdsSubSystemImportTarget
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
 - IVdsSubSystemImportTarget
 - vds/IVdsSubSystemImportTarget
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
 - IVdsSubSystemImportTarget
---

# IVdsSubSystemImportTarget interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and configure the default VSS import target for the 
   subsystem.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemImportTarget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsSubSystemImportTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemImportTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdssubsystemimporttarget-getimporttarget">GetImportTarget</a>
</td>
<td align="left" width="63%">
Returns the VSS import target for the computer for this subsystem.</p> (Inherited from <b>IVdsSubSystemImportTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdssubsystemimporttarget-setimporttarget">SetImportTarget</a>
</td>
<td align="left" width="63%">
Sets the VSS import target for the computer for this subsystem.</p> (Inherited from <b>IVdsSubSystemImportTarget</b>)</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>

