---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGIDebug1 interface


## -description


Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the  <b>IDXGIDebug1</b> interface in Windows Store apps. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDebug1</b> interface inherits from <a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a>. <b>IDXGIDebug1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDebug1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A96849C-D2DB-49F2-AEE9-CDC63F970077">DisableLeakTrackingForThread</a>
</td>
<td align="left" width="63%">
Stops tracking leaks for the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A6CE092E-389C-4DFE-A7A6-10CA96A0C1F4">EnableLeakTrackingForThread</a>
</td>
<td align="left" width="63%">
Starts tracking leaks for the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ACC57DDE-F019-415F-AAFA-E56ACE4F4197">IsLeakTrackingEnabledForThread</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether leak tracking is turned on for the current thread.

</td>
</tr>
</table> 


## -remarks



Call the <a href="https://msdn.microsoft.com/0FE0EAF5-3ADC-426F-9DA9-FEDEC519EEF0">DXGIGetDebugInterface1</a> function to obtain the <b>IDXGIDebug1</b> interface.

The <b>IDXGIDebug1</b> interface can be used only if the debug layer is turned on. For more info, see <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">Debug Layer</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/0FE0EAF5-3ADC-426F-9DA9-FEDEC519EEF0">DXGIGetDebugInterface1</a>



<a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a>
 

 

