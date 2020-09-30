---
UID: NN:uiautomationclient.IUIAutomationCustomNavigationPattern
title: IUIAutomationCustomNavigationPattern (uiautomationclient.h)
description: Exposes a method to support access by a Microsoft UI Automation client to controls that support a custom navigation order.
helpviewer_keywords: ["IUIAutomationCustomNavigationPattern","IUIAutomationCustomNavigationPattern interface [Windows Accessibility]","IUIAutomationCustomNavigationPattern interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationCustomNavigationPattern","winauto.uiauto_IUIAutomationCustomNavigationPattern"]
old-location: winauto\uiauto_IUIAutomationCustomNavigationPattern.htm
tech.root: WinAuto
ms.assetid: 0FF8604E-DD0E-4243-9B7E-219A26ACAC9C
ms.date: 12/05/2018
ms.keywords: IUIAutomationCustomNavigationPattern, IUIAutomationCustomNavigationPattern interface [Windows Accessibility], IUIAutomationCustomNavigationPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationCustomNavigationPattern, winauto.uiauto_IUIAutomationCustomNavigationPattern
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationCustomNavigationPattern
 - uiautomationclient/IUIAutomationCustomNavigationPattern
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationCustomNavigationPattern
---

# IUIAutomationCustomNavigationPattern interface


## -description

Exposes a method to support access by a Microsoft UI Automation client to controls that support a custom navigation order.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationCustomNavigationPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationCustomNavigationPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationCustomNavigationPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationcustomnavigationpattern-navigate">Navigate</a>
</td>
<td align="left" width="63%">
Gets the next element in the specified direction within the logical UI tree.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection</a>