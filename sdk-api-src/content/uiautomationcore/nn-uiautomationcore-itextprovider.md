---
UID: NN:uiautomationcore.ITextProvider
title: ITextProvider (uiautomationcore.h)
description: Provides access to controls that contain text.
helpviewer_keywords: ["ITextProvider","ITextProvider interface [Windows Accessibility]","ITextProvider interface [Windows Accessibility]","described","uiauto.uiauto_ITextProvider","uiauto_ITextProvider","uiautomationcore/ITextProvider","winauto.uiauto_ITextProvider"]
old-location: winauto\uiauto_ITextProvider.htm
tech.root: WinAuto
ms.assetid: 8bd53f1e-731f-420b-a529-ca3f6c3fd97c
ms.date: 12/05/2018
ms.keywords: ITextProvider, ITextProvider interface [Windows Accessibility], ITextProvider interface [Windows Accessibility],described, uiauto.uiauto_ITextProvider, uiauto_ITextProvider, uiautomationcore/ITextProvider, winauto.uiauto_ITextProvider
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
 - ITextProvider
 - uiautomationcore/ITextProvider
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
 - ITextProvider
---

# ITextProvider interface


## -description

Provides access to controls that contain text.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITextProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-getvisibleranges">GetVisibleRanges</a>
</td>
<td align="left" width="63%">
Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild">RangeFromChild</a>
</td>
<td align="left" width="63%">
Retrieves a text range enclosing a child element such as an image, hyperlink, or other embedded object. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefrompoint">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Returns the degenerate (empty) text range nearest to the specified screen coordinates. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-get_documentrange">DocumentRange</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a text range that encloses the main text of a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-get_supportedtextselection">SupportedTextSelection</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of text selection that is supported by the control.
        

</td>
</tr>
</table>

## -remarks

Implemented on a Microsoft UI Automation provider that must support the <a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text</a> control pattern.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2">ITextProvider2</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>