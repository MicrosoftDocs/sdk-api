---
UID: NN:vsprov.IVssHardwareSnapshotProvider
title: IVssHardwareSnapshotProvider (vsprov.h)
author: windows-sdk-content
description: Contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the shadow copy process, and transport LUNs on a SAN.
old-location: base\ivsshardwaresnapshotprovider.htm
tech.root: VSS
ms.assetid: 97fbb6bf-110e-4393-bf25-1ec378b91bdc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProvider, IVssHardwareSnapshotProvider interface [VSS], IVssHardwareSnapshotProvider interface [VSS],described, base.ivsshardwaresnapshotprovider, vsprov/IVssHardwareSnapshotProvider
ms.topic: interface
f1_keywords:
- vsprov/IVssHardwareSnapshotProvider
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VsProv.h
api_name:
- IVssHardwareSnapshotProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssHardwareSnapshotProvider interface


## -description


The <b>IVssHardwareSnapshotProvider</b> 
   interface contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the 
   shadow copy process, and transport LUNs on a SAN. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssHardwareSnapshotProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssHardwareSnapshotProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssHardwareSnapshotProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported">AreLunsSupported</a>
</td>
<td align="left" width="63%">
Determines whether the hardware provider supports shadow copy creation for all LUNs that contribute to the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
Called for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-fillinluninfo">FillInLunInfo</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns">GetTargetLuns</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to initialize the <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures for the newly created shadow copy LUNs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-locateluns">LocateLuns</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to make the shadow copy LUNs visible to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-onlunempty">OnLunEmpty</a>
</td>
<td align="left" width="63%">
Called whenever VSS determines that a shadow copy LUN contains no interesting data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

