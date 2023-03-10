---
UID: NF:uiautomationcore.IWindowProvider.WaitForInputIdle
title: IWindowProvider::WaitForInputIdle (uiautomationcore.h)
description: Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first. (IWindowProvider.WaitForInputIdle)
helpviewer_keywords: ["IWindowProvider interface [Windows Accessibility]","WaitForInputIdle method","IWindowProvider.WaitForInputIdle","IWindowProvider::WaitForInputIdle","WaitForInputIdle","WaitForInputIdle method [Windows Accessibility]","WaitForInputIdle method [Windows Accessibility]","IWindowProvider interface","uiauto.uiauto_IWindowProvider_WaitForInputIdle","uiauto_IWindowProvider_WaitForInputIdle","uiautomationcore/IWindowProvider::WaitForInputIdle","winauto.uiauto_IWindowProvider_WaitForInputIdle"]
old-location: winauto\uiauto_IWindowProvider_WaitForInputIdle.htm
tech.root: WinAuto
ms.assetid: 787f8309-09aa-4e6a-bfbc-fc03b917ead4
ms.date: 12/05/2018
ms.keywords: IWindowProvider interface [Windows Accessibility],WaitForInputIdle method, IWindowProvider.WaitForInputIdle, IWindowProvider::WaitForInputIdle, WaitForInputIdle, WaitForInputIdle method [Windows Accessibility], WaitForInputIdle method [Windows Accessibility],IWindowProvider interface, uiauto.uiauto_IWindowProvider_WaitForInputIdle, uiauto_IWindowProvider_WaitForInputIdle, uiautomationcore/IWindowProvider::WaitForInputIdle, winauto.uiauto_IWindowProvider_WaitForInputIdle
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
 - IWindowProvider::WaitForInputIdle
 - uiautomationcore/IWindowProvider::WaitForInputIdle
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
 - IWindowProvider.WaitForInputIdle
---

# IWindowProvider::WaitForInputIdle


## -description

Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.

## -parameters

### -param milliseconds [in]

Type: <b>int</b>

The amount of time, in milliseconds, to wait for the associated process to become idle. 
                The maximum is Int32.MaxValue.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if the window has entered the idle state; <b>FALSE</b> if the time-out occurred. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is typically used in conjunction with the handling of a <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_Window_WindowOpenedEventId</a>.
        The implementation is dependent on the underlying application framework; 
        therefore this method might return some time after the window is ready for user input. 
        The calling code should not rely on this method to ascertain exactly when the window has become idle. 
        Use the value of <i>pRetVal</i> to determine if the window is ready for input or if the method timed out.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iwindowprovider">IWindowProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
