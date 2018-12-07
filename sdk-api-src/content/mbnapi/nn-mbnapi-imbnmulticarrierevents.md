---
UID: NN:mbnapi.IMbnMultiCarrierEvents
title: IMbnMultiCarrierEvents
author: windows-sdk-content
description: This interface is a notification interface used to handle asynchronous IMbnMultiCarrier method calls.
old-location: mbn\imbnmulticarrierevents.htm
tech.root: mbn
ms.assetid: F7CAF21B-F487-4F35-806B-312B5246C1B2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnMultiCarrierEvents, IMbnMultiCarrierEvents interface [Microsoft Broadband Networks], IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],described, mbn.imbnmulticarrierevents, mbnapi/IMbnMultiCarrierEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnMultiCarrierEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnMultiCarrierEvents interface


## -description


This interface is a notification interface used to handle asynchronous <a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a> method calls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnMultiCarrierEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnMultiCarrierEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnMultiCarrierEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76B5349E-EA51-422D-81BC-A93B85FBCF90">OnCurrentCellularClassChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/8DA29C25-3866-4BCA-8591-F8408A1C1401">GetCurrentCellularClass</a> operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5701E0EB-FBDC-4791-97AA-B31F87763854">OnInterfaceCapabilityChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation that updates the interface capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B2E7C42B-32B0-47D1-AA88-8A22B379B500">OnPreferredProvidersChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/91D27D4D-5838-4D6D-BECF-B336B9F3B52A">GetPreferredProviders</a> operation and a change in a device's preferred provider list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EF1A39DB-351F-4105-BE56-C59477A67EC6">OnScanNetworkComplete</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a> operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6D0B5692-4D8C-45B1-B0AF-D507FD752B1F">OnSetHomeProviderComplete</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://msdn.microsoft.com/9FDC1B01-4768-4621-9B0E-6EC9AB4275A9">SetHomeProvider</a> operation.

</td>
</tr>
</table> 

