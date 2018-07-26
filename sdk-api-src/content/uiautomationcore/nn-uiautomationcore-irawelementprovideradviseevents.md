---
UID: NN:uiautomationcore.IRawElementProviderAdviseEvents
title: IRawElementProviderAdviseEvents
author: windows-sdk-content
description: Exposes methods that are called to notify the root element of a fragment when a Microsoft UI Automation client application begins or ends listening for events on that fragment.
old-location: winauto\uiauto_IRawElementProviderAdviseEvents.htm
old-project: WinAuto
ms.assetid: 6bc21bf8-8fe6-4b46-a79a-409c94a9bd42
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IRawElementProviderAdviseEvents, IRawElementProviderAdviseEvents interface [Windows Accessibility], IRawElementProviderAdviseEvents interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderAdviseEvents, uiauto_IRawElementProviderAdviseEvents, uiautomationcore/IRawElementProviderAdviseEvents, winauto.uiauto_IRawElementProviderAdviseEvents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderAdviseEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderAdviseEvents interface


## -description


Exposes methods that are called to notify the root element of a fragment 
		when a Microsoft UI Automation client application begins or ends listening for events on that fragment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderAdviseEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRawElementProviderAdviseEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b5902d9b-e008-4b91-933e-82506718eecd">AdviseEventAdded</a>
</td>
<td align="left" width="63%">
Notifies the UI Automation provider when a UI Automation client begins listening for a specific event, including a 
		property-changed event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42c9aeeb-dc08-4c13-ae86-2c0fb93e5c17">AdviseEventRemoved</a>
</td>
<td align="left" width="63%">
Notifies the UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event. 


</td>
</tr>
</table> 


## -remarks



Implementation of this interface is optional. It can be used to improve performance by raising events only when they are being listened for.
	

Similar to implementing reference counting in Component Object Model (COM) programming, it is important for UI Automation providers to treat the <a href="https://msdn.microsoft.com/b5902d9b-e008-4b91-933e-82506718eecd">AdviseEventAdded</a> and <a href="https://msdn.microsoft.com/42c9aeeb-dc08-4c13-ae86-2c0fb93e5c17">AdviseEventRemoved</a> methods like the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> and <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> methods of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.
As long as <b>AdviseEventAdded</b> has been called more times than <b>AdviseEventRemoved</b> for a specific event or property, the provider should continue to raise corresponding events, because some clients are still listening. Alternatively, UI Automation providers can use the <a href="https://msdn.microsoft.com/66b5d6b9-b51a-4848-b6e4-bd4c73b07f18">UiaClientsAreListening</a> function to determine if at least one client is listening and, if so, raise all appropriate events. 



