---
UID: NN:uiautomationclient.IUIAutomationElementArray
title: IUIAutomationElementArray (uiautomationclient.h)
description: Represents a collection of UI Automation elements.
helpviewer_keywords: ["IUIAutomationElementArray","IUIAutomationElementArray interface [Windows Accessibility]","IUIAutomationElementArray interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationElementArray","uiauto_IUIAutomationElementArray","uiautomationclient/IUIAutomationElementArray","winauto.uiauto_IUIAutomationElementArray"]
old-location: winauto\uiauto_IUIAutomationElementArray.htm
tech.root: WinAuto
ms.assetid: 7ecf585c-ff3b-4f89-8a7d-e2de66650ab4
ms.date: 12/05/2018
ms.keywords: IUIAutomationElementArray, IUIAutomationElementArray interface [Windows Accessibility], IUIAutomationElementArray interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationElementArray, uiauto_IUIAutomationElementArray, uiautomationclient/IUIAutomationElementArray, winauto.uiauto_IUIAutomationElementArray
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
 - IUIAutomationElementArray
 - uiautomationclient/IUIAutomationElementArray
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
 - IUIAutomationElementArray
---

# IUIAutomationElementArray interface


## -description

Represents a collection of UI Automation elements.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElementArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationElementArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationElementArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelementarray-getelement">GetElement</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElementArray</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelementarray-get_length">Length</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of elements in the collection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>