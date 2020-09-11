---
UID: NN:uiautomationclient.IUIAutomationTextPattern
title: IUIAutomationTextPattern (uiautomationclient.h)
description: Provides access to a control that contains text.
helpviewer_keywords: ["IUIAutomationTextPattern","IUIAutomationTextPattern interface [Windows Accessibility]","IUIAutomationTextPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTextPattern","uiauto_IUIAutomationTextPattern","uiautomationclient/IUIAutomationTextPattern","winauto.uiauto_IUIAutomationTextPattern"]
old-location: winauto\uiauto_IUIAutomationTextPattern.htm
tech.root: WinAuto
ms.assetid: ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern, IUIAutomationTextPattern interface [Windows Accessibility], IUIAutomationTextPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTextPattern, uiauto_IUIAutomationTextPattern, uiautomationclient/IUIAutomationTextPattern, winauto.uiauto_IUIAutomationTextPattern
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationTextPattern
 - uiautomationclient/IUIAutomationTextPattern
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
 - IUIAutomationTextPattern
---

# IUIAutomationTextPattern interface


## -description

Provides access to a control that contains text.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTextPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTextPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-getselection">GetSelection</a>
</td>
<td align="left" width="63%">
Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges">GetVisibleRanges</a>
</td>
<td align="left" width="63%">
Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild">RangeFromChild</a>
</td>
<td align="left" width="63%">
Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-rangefrompoint">RangeFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange">DocumentRange</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection">SupportedTextSelection</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that specifies the type of text selection that is supported by the control.
        

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

