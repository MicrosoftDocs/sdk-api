---
UID: NN:uiautomationcore.IRangeValueProvider
title: IRangeValueProvider (uiautomationcore.h)
description: Provides access to controls that can be set to a value within a range.
helpviewer_keywords: ["IRangeValueProvider","IRangeValueProvider interface [Windows Accessibility]","IRangeValueProvider interface [Windows Accessibility]","described","uiauto.uiauto_IRangeValueProvider","uiauto_IRangeValueProvider","uiautomationcore/IRangeValueProvider","winauto.uiauto_IRangeValueProvider"]
old-location: winauto\uiauto_IRangeValueProvider.htm
tech.root: WinAuto
ms.assetid: 1e9e39f9-e728-4ed6-bc62-80d3bbe6302d
ms.date: 12/05/2018
ms.keywords: IRangeValueProvider, IRangeValueProvider interface [Windows Accessibility], IRangeValueProvider interface [Windows Accessibility],described, uiauto.uiauto_IRangeValueProvider, uiauto_IRangeValueProvider, uiautomationcore/IRangeValueProvider, winauto.uiauto_IRangeValueProvider
f1_keywords:
- uiautomationcore/IRangeValueProvider
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
- IRangeValueProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRangeValueProvider interface


## -description


Provides access to controls that can be set to a value within a range.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeValueProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRangeValueProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRangeValueProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRangeValueProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_isreadonly">IsReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the value of a control is read-only. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_largechange">LargeChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the value that is added to or subtracted from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_value">IRangeValueProvider::Value</a> 
        property when a large change is made, such as when the PAGE DOWN key is pressed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_maximum">Maximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the maximum range value supported by the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_minimum">Minimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the minimum range value supported by the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_smallchange">SmallChange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the value that is added to or subtracted from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_value">IRangeValueProvider::Value</a> property 
        when a small change is made, such as when an arrow key is pressed.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irangevalueprovider-get_value">Value</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the value of the control.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingrangevalue">RangeValue</a> control pattern.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

