---
UID: NN:dxgi1_4.IDXGIAdapter3
title: IDXGIAdapter3
author: windows-sdk-content
description: This interface adds some memory residency methods, for budgeting and reserving physical memory.
old-location: direct3ddxgi\idxgiadapter3.htm
old-project: direct3ddxgi
ms.assetid: 547840B4-4AAB-4049-8D79-BD34BA4D32CD
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IDXGIAdapter3, IDXGIAdapter3 interface [DXGI], IDXGIAdapter3 interface [DXGI],described, direct3ddxgi.idxgiadapter3, dxgi1_4/IDXGIAdapter3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIAdapter3 interface


## -description


This interface adds some memory residency methods, for budgeting and reserving physical memory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIAdapter3</b> interface inherits from <a href="https://msdn.microsoft.com/9AAD133C-CE40-498B-827F-2B35C7C15B8C">IDXGIAdapter2</a>. <b>IDXGIAdapter3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">QueryVideoMemoryInfo</a>
</td>
<td align="left" width="63%">

          This method informs the process of the current budget and process usage.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/789E6EA1-C590-44F6-A474-851E5CF437A5">RegisterHardwareContentProtectionTeardownStatusEvent</a>
</td>
<td align="left" width="63%">
Registers to receive notification of hardware content protection teardown events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58ACCDE6-CB33-4BCE-9B15-84F60AC7B905">RegisterVideoMemoryBudgetChangeNotificationEvent</a>
</td>
<td align="left" width="63%">
This method establishes a correlation between a CPU synchronization object and the budget change event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D17F57F-9FFA-4B5C-98B6-33E5B3982A63">SetVideoMemoryReservation</a>
</td>
<td align="left" width="63%">

          This method sends the minimum required physical memory for an application, to the OS.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/821F8BFA-FD11-4E3E-BE5A-05A1F1002EE6">UnregisterHardwareContentProtectionTeardownStatus</a>
</td>
<td align="left" width="63%">
Unregisters an event to stop it from receiving notification of hardware content protection teardown events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11695B9E-75B5-44BF-BC09-D377BCEDA341">UnregisterVideoMemoryBudgetChangeNotification</a>
</td>
<td align="left" width="63%">
This method stops notifying a CPU synchronization object whenever a budget change occurs. An application may switch back to polling the information regularly.

</td>
</tr>
</table> 


## -remarks



For more details, refer to the <a href="https://msdn.microsoft.com/956F80D7-EEC8-4D88-B251-EE325614F31E">Residency</a> section of the D3D12 documentation.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/9AAD133C-CE40-498B-827F-2B35C7C15B8C">IDXGIAdapter2</a>
 

 

