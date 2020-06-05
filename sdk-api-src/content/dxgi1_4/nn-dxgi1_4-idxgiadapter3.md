---
UID: NN:dxgi1_4.IDXGIAdapter3
title: IDXGIAdapter3 (dxgi1_4.h)
description: This interface adds some memory residency methods, for budgeting and reserving physical memory.helpviewer_keywords: ["IDXGIAdapter3","IDXGIAdapter3 interface [DXGI]","IDXGIAdapter3 interface [DXGI]","described","direct3ddxgi.idxgiadapter3","dxgi1_4/IDXGIAdapter3"]
old-location: direct3ddxgi\idxgiadapter3.htm
tech.root: direct3ddxgi
ms.assetid: 547840B4-4AAB-4049-8D79-BD34BA4D32CD
ms.date: 12/05/2018
ms.keywords: IDXGIAdapter3, IDXGIAdapter3 interface [DXGI], IDXGIAdapter3 interface [DXGI],described, direct3ddxgi.idxgiadapter3, dxgi1_4/IDXGIAdapter3
f1_keywords:
- dxgi1_4/IDXGIAdapter3
dev_langs:
- c++
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dxgi.dll
api_name:
- IDXGIAdapter3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIAdapter3 interface


## -description


This interface adds some memory residency methods, for budgeting and reserving physical memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiadapter2">IDXGIAdapter2</a>. <b>IDXGIAdapter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIAdapter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">QueryVideoMemoryInfo</a>
</td>
<td align="left" width="63%">
This method informs the process of the current budget and process usage.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">RegisterHardwareContentProtectionTeardownStatusEvent</a>
</td>
<td align="left" width="63%">
Registers to receive notification of hardware content protection teardown events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">RegisterVideoMemoryBudgetChangeNotificationEvent</a>
</td>
<td align="left" width="63%">
This method establishes a correlation between a CPU synchronization object and the budget change event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-setvideomemoryreservation">SetVideoMemoryReservation</a>
</td>
<td align="left" width="63%">
This method sends the minimum required physical memory for an application, to the OS.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-unregisterhardwarecontentprotectionteardownstatus">UnregisterHardwareContentProtectionTeardownStatus</a>
</td>
<td align="left" width="63%">
Unregisters an event to stop it from receiving notification of hardware content protection teardown events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-unregistervideomemorybudgetchangenotification">UnregisterVideoMemoryBudgetChangeNotification</a>
</td>
<td align="left" width="63%">
This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.

</td>
</tr>
</table> 


## -remarks



For more details, refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/residency">Residency</a> section of the D3D12 documentation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiadapter2">IDXGIAdapter2</a>
 

 

