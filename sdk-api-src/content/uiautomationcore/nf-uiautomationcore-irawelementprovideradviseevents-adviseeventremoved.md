---
UID: NF:uiautomationcore.IRawElementProviderAdviseEvents.AdviseEventRemoved
title: IRawElementProviderAdviseEvents::AdviseEventRemoved
author: windows-sdk-content
description: Notifies the Microsoft UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event.
old-location: winauto\uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved.htm
tech.root: WinAuto
ms.assetid: 42c9aeeb-dc08-4c13-ae86-2c0fb93e5c17
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AdviseEventRemoved, AdviseEventRemoved method [Windows Accessibility], AdviseEventRemoved method [Windows Accessibility],IRawElementProviderAdviseEvents interface, IRawElementProviderAdviseEvents interface [Windows Accessibility],AdviseEventRemoved method, IRawElementProviderAdviseEvents.AdviseEventRemoved, IRawElementProviderAdviseEvents::AdviseEventRemoved, uiauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved, uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved, uiautomationcore/IRawElementProviderAdviseEvents::AdviseEventRemoved, winauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderAdviseEvents.AdviseEventRemoved
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderAdviseEvents::AdviseEventRemoved


## -description


Notifies the Microsoft UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event. 



## -parameters




### -param eventId [in]

Type: <b>EVENTID</b>

The identifier of the event being removed. For a list of event IDs, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -param propertyIDs [in]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the identifiers of the properties being removed, or <b>NULL</b>if the event listener being removed is not listening for property events.



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method enables the provider to reduce overhead by raising only events that are being listened for.

It is important for UI Automation providers to treat the <b>IRawElementProviderAdviseEvents::AdviseEventRemoved</b> like the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. As long as <a href="https://msdn.microsoft.com/b5902d9b-e008-4b91-933e-82506718eecd">AdviseEventAdded</a> has been called more times than <b>AdviseEventRemoved</b> for a specific event or property, the provider should continue to raise corresponding events, because some clients are still listening. Alternatively, UI Automation providers can use the <a href="https://msdn.microsoft.com/66b5d6b9-b51a-4848-b6e4-bd4c73b07f18">UiaClientsAreListening</a> function to determine if at least one client is listening and, if so, raise all appropriate events. 




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6bc21bf8-8fe6-4b46-a79a-409c94a9bd42">IRawElementProviderAdviseEvents</a>



<b>Reference</b>
 

 

