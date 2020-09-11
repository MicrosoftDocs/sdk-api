---
UID: NN:uiautomationcore.IAccessibleEx
title: IAccessibleEx (uiautomationcore.h)
description: Exposes methods that are called by Microsoft UI Automation to retrieve extra information about a control that supports Microsoft Active Accessibility.
helpviewer_keywords: ["IAccessibleEx","IAccessibleEx interface [Windows Accessibility]","IAccessibleEx interface [Windows Accessibility]","described","uiauto.uiauto_IAccessibleEx","uiauto_IAccessibleEx","uiautomationcore/IAccessibleEx","winauto.uiauto_IAccessibleEx"]
old-location: winauto\uiauto_IAccessibleEx.htm
tech.root: WinAuto
ms.assetid: 90211503-a73c-4380-be96-0be40ad29382
ms.date: 12/05/2018
ms.keywords: IAccessibleEx, IAccessibleEx interface [Windows Accessibility], IAccessibleEx interface [Windows Accessibility],described, uiauto.uiauto_IAccessibleEx, uiauto_IAccessibleEx, uiautomationcore/IAccessibleEx, winauto.uiauto_IAccessibleEx
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAccessibleEx
 - uiautomationcore/IAccessibleEx
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
 - IAccessibleEx
---

# IAccessibleEx interface


## -description

Exposes methods that are called by Microsoft UI Automation to retrieve extra information about a control that supports Microsoft Active Accessibility.

## -inheritance

The **IAccessibleEx** interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. **IAccessibleEx** also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessibleex-convertreturnedelement">ConvertReturnedElement</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IAccessibleEx</b> interface of an element returned as a property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair">GetIAccessiblePair</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface and child ID for this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessibleex-getobjectforchild">GetObjectForChild</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IAccessibleEx</b> interface representing the specified child of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessibleex-getruntimeid">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the runtime identifier of this element.

</td>
</tr>
</table>

## -remarks

This interface can be implemented on custom controls that also implement the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface, to provide added support for UI Automation without the cost of a full UI Automation provider implementation.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-usingiaccessibleex">Adding UI Automation Functionality to Active Accessibility Servers</a>

