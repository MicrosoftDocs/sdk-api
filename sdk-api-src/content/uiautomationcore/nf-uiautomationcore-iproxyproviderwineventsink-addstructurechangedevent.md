---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddStructureChangedEvent
title: IProxyProviderWinEventSink::AddStructureChangedEvent
author: windows-sdk-content
description: Raises an event to notify clients that the structure of the UI Automation tree has changed.
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent.htm
old-project: WinAuto
ms.assetid: 03be09a6-da4d-4071-bd7c-df79688c20d3
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: AddStructureChangedEvent, AddStructureChangedEvent method [Windows Accessibility], AddStructureChangedEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddStructureChangedEvent method, IProxyProviderWinEventSink.AddStructureChangedEvent, IProxyProviderWinEventSink::AddStructureChangedEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent, uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent, uiautomationcore/IProxyProviderWinEventSink::AddStructureChangedEvent, winauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent
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
 - IProxyProviderWinEventSink.AddStructureChangedEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IProxyProviderWinEventSink::AddStructureChangedEvent


## -description


Raises an event to notify clients that the structure of the UI Automation tree has changed.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

A pointer to the provider of the element that is raising the event.


### -param structureChangeType [in]

Type: <b><a href="https://msdn.microsoft.com/abaf9551-40c4-4ab6-adb7-b619f3bc9745">StructureChangeType</a></b>

The type of structure change that occurred.


### -param runtimeId [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A pointer to the runtime identifiers of the elements that are affected. These IDs enable applications to identify elements that have been removed and are no longer represented by <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interfaces.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a>



<b>Reference</b>
 

 

