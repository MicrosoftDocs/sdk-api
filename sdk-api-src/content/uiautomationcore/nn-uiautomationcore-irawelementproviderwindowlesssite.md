---
UID: NN:uiautomationcore.IRawElementProviderWindowlessSite
title: IRawElementProviderWindowlessSite (uiautomationcore.h)
author: windows-sdk-content
description: A Microsoft ActiveX control site implements this interface to enable a Microsoft UI Automation-enabled ActiveX control to express its accessibility.
old-location: winauto\uiauto_IRawElementProviderWindowlessSite.htm
tech.root: WinAuto
ms.assetid: E6BE069B-C639-4578-9E5F-8CFE1267A847
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRawElementProviderWindowlessSite, IRawElementProviderWindowlessSite interface [Windows Accessibility], IRawElementProviderWindowlessSite interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderWindowlessSite, winauto.uiauto_IRawElementProviderWindowlessSite
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IRawElementProviderWindowlessSite"
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
 - IRawElementProviderWindowlessSite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRawElementProviderWindowlessSite interface


## -description


A Microsoft ActiveX control site implements this interface to enable a Microsoft UI Automation-enabled ActiveX control to express its accessibility.   This interface enables the control container to provide an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> pointer for the parent or siblings of the windowless ActiveX control, and to provide a runtime ID that is unique to the control site.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderWindowlessSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderWindowlessSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderWindowlessSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getadjacentfragment">GetAdjacentFragment</a>
</td>
<td align="left" width="63%">
Retrieves a fragment pointer for a fragment that is adjacent to the windowless ActiveX control  owned by this control site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderwindowlesssite-getruntimeidprefix">GetRuntimeIdPrefix</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation runtime ID that is unique to the windowless ActiveX control site. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>
 

 

