---
UID: NN:uiautomationcore.IAccessibleHostingElementProviders
title: IAccessibleHostingElementProviders (uiautomationcore.h)
description: A Microsoft Active Accessibility object implements this interface when the object is the root of an accessibility tree that includes windowless Microsoft ActiveX controls that implement Microsoft UI Automation.
old-location: winauto\iaccessiblehostingelementproviders.htm
tech.root: WinAuto
ms.assetid: 8D974311-25CB-4D49-B907-2984D0DA58D7
ms.date: 12/05/2018
ms.keywords: IAccessibleHostingElementProviders, IAccessibleHostingElementProviders interface [Windows Accessibility], IAccessibleHostingElementProviders interface [Windows Accessibility],described, uiautomationcore/IAccessibleHostingElementProviders, winauto.iaccessiblehostingelementproviders
f1_keywords:
- uiautomationcore/IAccessibleHostingElementProviders
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IAccessibleHostingElementProviders
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessibleHostingElementProviders interface


## -description


A Microsoft Active Accessibility object implements this interface when the object is the root of an accessibility tree that includes windowless Microsoft ActiveX controls that implement Microsoft UI Automation.  Because Microsoft Active Accessibility and UI Automation use different interfaces, this interface enables a client to discover the list of hosted windowless ActiveX controls that support  UI Automation in case the client needs to treat them differently.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleHostingElementProviders</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessibleHostingElementProviders</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleHostingElementProviders</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessiblehostingelementproviders-getembeddedfragmentroots">GetEmbeddedFragmentRoots</a>
</td>
<td align="left" width="63%">
Retrieves the  Microsoft Active Accessibility providers of  all windowless ActiveX controls that have a UI Automation provider implementation, and are hosted in a Microsoft Active Accessibility object that implements the <b>IAccessibleHostingElementProviders</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iaccessiblehostingelementproviders-getobjectidforprovider">GetObjectIdForProvider</a>
</td>
<td align="left" width="63%">
Retrieves the object ID associated with a contained windowless ActiveX control that implements UI Automation.  

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles">IRawElementProviderHostingAccessibles</a>
 

 

