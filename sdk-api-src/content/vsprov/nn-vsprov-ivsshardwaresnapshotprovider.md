---
UID: NN:vsprov.IVssHardwareSnapshotProvider
title: IVssHardwareSnapshotProvider
author: windows-sdk-content
description: Contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the shadow copy process, and transport LUNs on a SAN.
old-location: base\ivsshardwaresnapshotprovider.htm
old-project: VSS
ms.assetid: 97fbb6bf-110e-4393-bf25-1ec378b91bdc
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssHardwareSnapshotProvider, IVssHardwareSnapshotProvider interface [VSS], IVssHardwareSnapshotProvider interface [VSS],described, base.ivsshardwaresnapshotprovider, vsprov/IVssHardwareSnapshotProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsProv.h
api_name:
-	IVssHardwareSnapshotProvider
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssHardwareSnapshotProvider interface


## -description


The <b>IVssHardwareSnapshotProvider</b> 
   interface contains the methods used by VSS to map volumes to LUNs, discover LUNs created during the 
   shadow copy process, and transport LUNs on a SAN. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssHardwareSnapshotProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssHardwareSnapshotProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f3615770-63a1-49eb-a3b9-b4d349fc33df">AreLunsSupported</a>
</td>
<td align="left" width="63%">
Determines whether the hardware provider supports shadow copy creation for all LUNs that contribute to the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a8bdffa-bb6e-425d-a708-1f31af302da9">BeginPrepareSnapshot</a>
</td>
<td align="left" width="63%">
Called for each shadow copy that is added to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e4e5942-5bc8-4b5e-a651-5bb354514994">FillInLunInfo</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/299020eb-0afd-41c8-9551-1275eff45fa1">GetTargetLuns</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to initialize the <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structures for the newly created shadow copy LUNs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a996875-a495-43c1-987e-67c31d0651c7">LocateLuns</a>
</td>
<td align="left" width="63%">
Prompts the hardware provider to make the shadow copy LUNs visible to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06a31704-9031-4ab9-84eb-685f6b648d27">OnLunEmpty</a>
</td>
<td align="left" width="63%">
Called whenever VSS determines that a shadow copy LUN contains no interesting data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

