---
UID: NN:uiautomationcore.IRawElementProviderSimple
title: IRawElementProviderSimple (uiautomationcore.h)
description: Defines methods and properties that expose simple UI elements.
helpviewer_keywords: ["IRawElementProviderSimple","IRawElementProviderSimple interface [Windows Accessibility]","IRawElementProviderSimple interface [Windows Accessibility]","described","uiauto.uiauto_IRawElementProviderSimple","uiauto_IRawElementProviderSimple","uiautomationcore/IRawElementProviderSimple","winauto.uiauto_IRawElementProviderSimple"]
old-location: winauto\uiauto_IRawElementProviderSimple.htm
tech.root: WinAuto
ms.assetid: f0ec6185-acd0-4df7-88f4-fd00747f98bf
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple, IRawElementProviderSimple interface [Windows Accessibility], IRawElementProviderSimple interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderSimple, uiauto_IRawElementProviderSimple, uiautomationcore/IRawElementProviderSimple, winauto.uiauto_IRawElementProviderSimple
f1_keywords:
- uiautomationcore/IRawElementProviderSimple
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IRawElementProviderSimple
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRawElementProviderSimple interface


## -description


Defines methods and properties that expose simple UI elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderSimple</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderSimple</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider">GetPatternProvider</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an object that provides support for a control pattern on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue">GetPropertyValue</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider">HostRawElementProvider</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions">ProviderOptions</a>


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
Providers for complex elements must also implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> and, if they 
			are root elements, <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>



<b>Reference</b>
 

 

