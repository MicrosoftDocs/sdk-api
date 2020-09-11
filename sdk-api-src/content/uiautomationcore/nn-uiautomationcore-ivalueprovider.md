---
UID: NN:uiautomationcore.IValueProvider
title: IValueProvider (uiautomationcore.h)
description: Provides access to controls that have an intrinsic value that does not span a range, and that can be represented as a string.
helpviewer_keywords: ["IValueProvider","IValueProvider interface [Windows Accessibility]","IValueProvider interface [Windows Accessibility]","described","uiauto.uiauto_IValueProvider","uiauto_IValueProvider","uiautomationcore/IValueProvider","winauto.uiauto_IValueProvider"]
old-location: winauto\uiauto_IValueProvider.htm
tech.root: WinAuto
ms.assetid: e6adbc23-dbfe-4dd2-82d9-66ce16de3338
ms.date: 12/05/2018
ms.keywords: IValueProvider, IValueProvider interface [Windows Accessibility], IValueProvider interface [Windows Accessibility],described, uiauto.uiauto_IValueProvider, uiauto_IValueProvider, uiautomationcore/IValueProvider, winauto.uiauto_IValueProvider
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValueProvider
 - uiautomationcore/IValueProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IValueProvider
---

# IValueProvider interface


## -description

Provides access 
        to controls that have an intrinsic value that does not span a range, and that can be represented as a string.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IValueProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IValueProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivalueprovider-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the value of control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivalueprovider-get_isreadonly">IsReadOnly</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivalueprovider-get_value">Value</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The value of the control.

</td>
</tr>
</table>

## -remarks

The value of the control may or may not be editable depending on the control and its settings.
        

Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingvalue">Value</a> control pattern.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>

