---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddAutomationEvent
title: IProxyProviderWinEventSink::AddAutomationEvent
author: windows-sdk-content
description: Raises a Microsoft UI Automation event.
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddAutomationEvent.htm
old-project: WinAuto
ms.assetid: c1730b6b-f399-4e1f-91d4-5d5e40835a74
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: AddAutomationEvent, AddAutomationEvent method [Windows Accessibility], AddAutomationEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddAutomationEvent method, IProxyProviderWinEventSink.AddAutomationEvent, IProxyProviderWinEventSink::AddAutomationEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent, uiauto_IProxyProviderWinEventSink_AddAutomationEvent, uiautomationcore/IProxyProviderWinEventSink::AddAutomationEvent, winauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
 - IProxyProviderWinEventSink.AddAutomationEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IProxyProviderWinEventSink::AddAutomationEvent


## -description


Raises a Microsoft UI Automation event.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

A pointer to the provider for the element that will raise the event.


### -param id [in]

Type: <b>EVENTID</b>

The identifier of the event that will be raised. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a>
 

 

