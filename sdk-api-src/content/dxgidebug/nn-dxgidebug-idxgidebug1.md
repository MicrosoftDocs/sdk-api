---
UID: NN:dxgidebug.IDXGIDebug1
title: IDXGIDebug1
author: windows-sdk-content
description: Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the IDXGIDebug1 interface in Windows Store apps.
old-location: direct3ddxgi\idxgidebug1.htm
old-project: direct3ddxgi
ms.assetid: 16D52CA2-1495-407C-9B88-CF4D4C90BAFA
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDXGIDebug1, IDXGIDebug1 interface [DXGI], IDXGIDebug1 interface [DXGI],described, direct3ddxgi.idxgidebug1, dxgidebug/IDXGIDebug1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGIDebug.dll
api_name:
-	IDXGIDebug1
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

