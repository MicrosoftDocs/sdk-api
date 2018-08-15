---
UID: NF:uiautomationcore.IRawElementProviderAdviseEvents.AdviseEventAdded
title: IRawElementProviderAdviseEvents::AdviseEventAdded
author: windows-sdk-content
description: Notifies the Microsoft UI Automation provider when a UI Automation client begins listening for a specific event, including a property-changed event.
old-location: winauto\uiauto_IRawElementProviderAdviseEvents_AdviseEventAdded.htm
old-project: WinAuto
ms.assetid: b5902d9b-e008-4b91-933e-82506718eecd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AdviseEventAdded, AdviseEventAdded method [Windows Accessibility], AdviseEventAdded method [Windows Accessibility],IRawElementProviderAdviseEvents interface, IRawElementProviderAdviseEvents interface [Windows Accessibility],AdviseEventAdded method, IRawElementProviderAdviseEvents.AdviseEventAdded, IRawElementProviderAdviseEvents::AdviseEventAdded, uiauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventAdded, uiauto_IRawElementProviderAdviseEvents_AdviseEventAdded, uiautomationcore/IRawElementProviderAdviseEvents::AdviseEventAdded, winauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventAdded
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
 - UIAutomationCore.h
api_name:
 - IRawElementProviderAdviseEvents.AdviseEventAdded
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderAdviseEvents::AdviseEventAdded


## -description


Notifies the Microsoft UI Automation provider when a UI Automation client begins listening for a specific event, including a 
		property-changed event.


## -parameters




### -param eventId [in]

Type: <b>EVENTID</b>

The identifier of the event being added. For a list of event IDs, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -param propertyIDs [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the identifiers of properties being added, or <b>NULL</b> if the event listener 
				being added is not listening for property events.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method enables the provider to reduce overhead by raising only events 
			that are being listened for.

It is important for UI Automation providers to treat the <b>IRawElementProviderAdviseEvents::AdviseEventAdded</b> like the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. As long as <b>AdviseEventAdded</b> has been called more times than <a href="https://msdn.microsoft.com/42c9aeeb-dc08-4c13-ae86-2c0fb93e5c17">AdviseEventRemoved</a> for a specific event or property, the provider should continue to raise corresponding events, because some clients are still listening. Alternatively, UI Automation providers can use the <a href="https://msdn.microsoft.com/66b5d6b9-b51a-4848-b6e4-bd4c73b07f18">UiaClientsAreListening</a> function to determine if at least one client is listening and, if so, raise all appropriate events. 




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6bc21bf8-8fe6-4b46-a79a-409c94a9bd42">IRawElementProviderAdviseEvents</a>



<b>Reference</b>
 

 

