---
UID: NN:vsprov.IVssHardwareSnapshotProviderEx
title: IVssHardwareSnapshotProviderEx
author: windows-sdk-content
description: Provides an additional method used by VSS to notify hardware providers of LUN state changes.
old-location: base\ivsshardwaresnapshotproviderex.htm
tech.root: VSS
ms.assetid: aaf94823-845b-49cb-8599-962229fef4cb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssHardwareSnapshotProviderEx, IVssHardwareSnapshotProviderEx interface, IVssHardwareSnapshotProviderEx interface,described, base.ivsshardwaresnapshotproviderex, vsprov/IVssHardwareSnapshotProviderEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssHardwareSnapshotProviderEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssHardwareSnapshotProviderEx interface


## -description


Provides an additional method used by VSS to notify hardware providers of LUN state changes. All hardware providers must support this 
   interface.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssHardwareSnapshotProviderEx</b> interface inherits from <a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>. <b>IVssHardwareSnapshotProviderEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssHardwareSnapshotProviderEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf95ba6c-b4da-4e9e-969e-58c492cf7901">GetProviderCapabilities</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7546eca0-db52-4c4b-9b5a-a3cfdf2a98af">OnLunStateChange</a>
</td>
<td align="left" width="63%">
The VSS service calls this method to notify hardware providers of a LUN state change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a92c992-a351-4d39-a370-f720e50dfbf3">OnReuseLuns</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27322ba0-e318-45d4-824e-8c81a18abd49">ResyncLuns</a>
</td>
<td align="left" width="63%">
The VSS service calls this method to notify hardware providers that a LUN resynchronization is needed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97fbb6bf-110e-4393-bf25-1ec378b91bdc">IVssHardwareSnapshotProvider</a>



<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

