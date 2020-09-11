---
UID: NN:uiautomationcore.IRawElementProviderAdviseEvents
title: IRawElementProviderAdviseEvents (uiautomationcore.h)
description: Exposes methods that are called to notify the root element of a fragment when a Microsoft UI Automation client application begins or ends listening for events on that fragment.
helpviewer_keywords: ["IRawElementProviderAdviseEvents","IRawElementProviderAdviseEvents interface [Windows Accessibility]","IRawElementProviderAdviseEvents interface [Windows Accessibility]","described","uiauto.uiauto_IRawElementProviderAdviseEvents","uiauto_IRawElementProviderAdviseEvents","uiautomationcore/IRawElementProviderAdviseEvents","winauto.uiauto_IRawElementProviderAdviseEvents"]
old-location: winauto\uiauto_IRawElementProviderAdviseEvents.htm
tech.root: WinAuto
ms.assetid: 6bc21bf8-8fe6-4b46-a79a-409c94a9bd42
ms.date: 12/05/2018
ms.keywords: IRawElementProviderAdviseEvents, IRawElementProviderAdviseEvents interface [Windows Accessibility], IRawElementProviderAdviseEvents interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderAdviseEvents, uiauto_IRawElementProviderAdviseEvents, uiautomationcore/IRawElementProviderAdviseEvents, winauto.uiauto_IRawElementProviderAdviseEvents
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
 - IRawElementProviderAdviseEvents
 - uiautomationcore/IRawElementProviderAdviseEvents
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
 - IRawElementProviderAdviseEvents
---

# IRawElementProviderAdviseEvents interface


## -description

Exposes methods that are called to notify the root element of a fragment 
		when a Microsoft UI Automation client application begins or ends listening for events on that fragment.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderAdviseEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderAdviseEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderAdviseEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded">AdviseEventAdded</a>
</td>
<td align="left" width="63%">
Notifies the UI Automation provider when a UI Automation client begins listening for a specific event, including a 
		property-changed event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved">AdviseEventRemoved</a>
</td>
<td align="left" width="63%">
Notifies the UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event. 


</td>
</tr>
</table>

## -remarks

Implementation of this interface is optional. It can be used to improve performance by raising events only when they are being listened for.
	

Similar to implementing reference counting in Component Object Model (COM) programming, it is important for UI Automation providers to treat the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded">AdviseEventAdded</a> and <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved">AdviseEventRemoved</a> methods like the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> and <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> methods of the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.
As long as <b>AdviseEventAdded</b> has been called more times than <b>AdviseEventRemoved</b> for a specific event or property, the provider should continue to raise corresponding events, because some clients are still listening. Alternatively, UI Automation providers can use the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaclientsarelistening">UiaClientsAreListening</a> function to determine if at least one client is listening and, if so, raise all appropriate events.

