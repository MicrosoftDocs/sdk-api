---
UID: NF:uiautomationcore.IWindowProvider.WaitForInputIdle
title: IWindowProvider::WaitForInputIdle
author: windows-sdk-content
description: Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.
old-location: winauto\uiauto_IWindowProvider_WaitForInputIdle.htm
tech.root: WinAuto
ms.assetid: 787f8309-09aa-4e6a-bfbc-fc03b917ead4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWindowProvider interface [Windows Accessibility],WaitForInputIdle method, IWindowProvider.WaitForInputIdle, IWindowProvider::WaitForInputIdle, WaitForInputIdle, WaitForInputIdle method [Windows Accessibility], WaitForInputIdle method [Windows Accessibility],IWindowProvider interface, uiauto.uiauto_IWindowProvider_WaitForInputIdle, uiauto_IWindowProvider_WaitForInputIdle, uiautomationcore/IWindowProvider::WaitForInputIdle, winauto.uiauto_IWindowProvider_WaitForInputIdle
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
 - IWindowProvider.WaitForInputIdle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Receives <b>TRUE</b> if the window has entered the idle state; <b>FALSE</b> if the time-out occurred. 
				This parameter is passed uninitialized. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is typically used in conjunction with the handling of a <a href="uiauto_event_ids.htm">UIA_Window_WindowOpenedEventId</a>.
        The implementation is dependent on the underlying application framework; 
        therefore this method might return some time after the window is ready for user input. 
        The calling code should not rely on this method to ascertain exactly when the window has become idle. 
        Use the value of <i>pRetVal</i> to determine if the window is ready for input or if the method timed out.






## -see-also




<a href="https://msdn.microsoft.com/cf09ad4e-fd5b-4304-b5fb-165205bff1f3">IWindowProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

