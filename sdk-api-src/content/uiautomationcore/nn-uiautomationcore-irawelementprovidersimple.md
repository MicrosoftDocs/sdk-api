---
UID: NN:uiautomationcore.IRawElementProviderSimple
title: IRawElementProviderSimple
author: windows-sdk-content
description: Defines methods and properties that expose simple UI elements.
old-location: winauto\uiauto_IRawElementProviderSimple.htm
old-project: WinAuto
ms.assetid: f0ec6185-acd0-4df7-88f4-fd00747f98bf
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IRawElementProviderSimple, IRawElementProviderSimple interface [Windows Accessibility], IRawElementProviderSimple interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderSimple, uiauto_IRawElementProviderSimple, uiautomationcore/IRawElementProviderSimple, winauto.uiauto_IRawElementProviderSimple
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderSimple
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderSimple interface


## -description


Defines methods and properties that expose simple UI elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderSimple</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRawElementProviderSimple</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRawElementProviderSimple</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8315c1d4-6347-462f-9c96-121f216faf88">GetPatternProvider</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an object that provides support for a control pattern on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451321">GetPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of a property supported by the UI Automation provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderSimple</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fcbd3dc8-5bc7-48ae-bc21-009876b3e673">HostRawElementProvider</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the host provider for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fd41bb43-bbf1-4022-9472-0ad2816074c6">ProviderOptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the type of UI Automation provider; for example, whether it is a client-side (proxy) or server-side provider.

</td>
</tr>
</table> 


## -remarks



This interface can be implemented on:
			

<ul>
<li>UI Automation provider for simple UI elements, such as buttons.</li>
<li>Providers that add or override properties or control patterns on a UI element that already has a provider.</li>
</ul>
Providers for complex elements must also implement <a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a> and, if they 
			are root elements, <a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>.




## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>



<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>



<b>Reference</b>
 

 

