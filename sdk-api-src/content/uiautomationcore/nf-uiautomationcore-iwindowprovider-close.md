---
UID: NF:uiautomationcore.IWindowProvider.Close
title: IWindowProvider::Close (uiautomationcore.h)
description: Attempts to close the window.
helpviewer_keywords: ["Close","Close method [Windows Accessibility]","Close method [Windows Accessibility]","IWindowProvider interface","IWindowProvider interface [Windows Accessibility]","Close method","IWindowProvider.Close","IWindowProvider::Close","uiauto.uiauto_IWindowProvider_Close","uiauto_IWindowProvider_Close","uiautomationcore/IWindowProvider::Close","winauto.uiauto_IWindowProvider_Close"]
old-location: winauto\uiauto_IWindowProvider_Close.htm
tech.root: WinAuto
ms.assetid: 3bfd7801-c296-4f59-8094-c13c8f044038
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Accessibility], Close method [Windows Accessibility],IWindowProvider interface, IWindowProvider interface [Windows Accessibility],Close method, IWindowProvider.Close, IWindowProvider::Close, uiauto.uiauto_IWindowProvider_Close, uiauto_IWindowProvider_Close, uiautomationcore/IWindowProvider::Close, winauto.uiauto_IWindowProvider_Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowProvider::Close
 - uiautomationcore/IWindowProvider::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IWindowProvider.Close
---

# IWindowProvider::Close


## -description

Attempts to close the window.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IWindowProvider::Close</b> must return immediately without blocking.
        

<b>IWindowProvider::Close</b> raises the <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_Window_WindowClosedEventId</a> 
        event. 
        If possible, the event should be raised after the control has completed its associated action. 
        

When called on a split pane control, this method will close the pane and remove 
        the associated split. 

This method may also close all other panes depending on implementation.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iwindowprovider">IWindowProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
