---
UID: NF:uiautomationcore.IWindowProvider.Close
title: IWindowProvider::Close
author: windows-sdk-content
description: Attempts to close the window.
old-location: winauto\uiauto_IWindowProvider_Close.htm
tech.root: WinAuto
ms.assetid: 3bfd7801-c296-4f59-8094-c13c8f044038
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: Close, Close method [Windows Accessibility], Close method [Windows Accessibility],IWindowProvider interface, IWindowProvider interface [Windows Accessibility],Close method, IWindowProvider.Close, IWindowProvider::Close, uiauto.uiauto_IWindowProvider_Close, uiauto_IWindowProvider_Close, uiautomationcore/IWindowProvider::Close, winauto.uiauto_IWindowProvider_Close
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
 - IWindowProvider.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowProvider::Close


## -description


Attempts to close the window.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IWindowProvider::Close</b> must return immediately without blocking.
        

<b>IWindowProvider::Close</b> raises the <a href="uiauto_event_ids.htm">UIA_Window_WindowClosedEventId</a> 
        event. 
        If possible, the event should be raised after the control has completed its associated action. 
        

When called on a split pane control, this method will close the pane and remove 
        the associated split. 

This method may also close all other panes depending on implementation.
        




## -see-also




<a href="https://msdn.microsoft.com/cf09ad4e-fd5b-4304-b5fb-165205bff1f3">IWindowProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

