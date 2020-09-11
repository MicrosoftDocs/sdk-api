---
UID: NN:uiautomationcore.IRawElementProviderHostingAccessibles
title: IRawElementProviderHostingAccessibles (uiautomationcore.h)
description: This interface is implemented by a Microsoft UI Automation provider when the provider is the root of an accessibility tree that includes windowless controls that support Microsoft Active Accessibility.
helpviewer_keywords: ["IRawElementProviderHostingAccessibles","IRawElementProviderHostingAccessibles interface [Windows Accessibility]","IRawElementProviderHostingAccessibles interface [Windows Accessibility]","described","uiautomationcore/IRawElementProviderHostingAccessibles","winauto.uiauto_IRawElementProviderHostingAccessibles"]
old-location: winauto\uiauto_IRawElementProviderHostingAccessibles.htm
tech.root: WinAuto
ms.assetid: 2DBD5B1A-127A-4D71-8117-5FCCE653698C
ms.date: 12/05/2018
ms.keywords: IRawElementProviderHostingAccessibles, IRawElementProviderHostingAccessibles interface [Windows Accessibility], IRawElementProviderHostingAccessibles interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderHostingAccessibles, winauto.uiauto_IRawElementProviderHostingAccessibles
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IRawElementProviderHostingAccessibles
 - uiautomationcore/IRawElementProviderHostingAccessibles
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
 - IRawElementProviderHostingAccessibles
---

# IRawElementProviderHostingAccessibles interface


## -description

This interface is implemented by a Microsoft UI Automation provider when the provider is the root of an accessibility tree that includes windowless controls that support Microsoft Active Accessibility.  Because UI Automation and Microsoft Active Accessibility use different interfaces, this interface enables a client to discover the list of hosted Microsoft Active Accessibility controls in case it needs to treat them differently.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderHostingAccessibles</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderHostingAccessibles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderHostingAccessibles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderhostingaccessibles-getembeddedaccessibles">GetEmbeddedAccessibles</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointers of the windowless ActiveX controls that are hosted by this provider.   

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessiblehostingelementproviders">IAccessibleHostingElementProviders</a>

