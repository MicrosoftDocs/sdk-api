---
UID: NF:uiautomationclient.IUIAutomationWindowPattern.WaitForInputIdle
title: IUIAutomationWindowPattern::WaitForInputIdle
author: windows-sdk-content
description: Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.
old-location: winauto\uiauto_IUIAutomationWindowPattern_WaitForInputIdle.htm
tech.root: WinAuto
ms.assetid: 2e08c3b1-6437-40ce-9dd3-2beb3e1f37fb
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IUIAutomationWindowPattern interface [Windows Accessibility],WaitForInputIdle method, IUIAutomationWindowPattern.WaitForInputIdle, IUIAutomationWindowPattern::WaitForInputIdle, WaitForInputIdle, WaitForInputIdle method [Windows Accessibility], WaitForInputIdle method [Windows Accessibility],IUIAutomationWindowPattern interface, uiauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle, uiauto_IUIAutomationWindowPattern_WaitForInputIdle, uiautomationclient/IUIAutomationWindowPattern::WaitForInputIdle, winauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - UIAutomationClient.h
api_name:
 - IUIAutomationWindowPattern.WaitForInputIdle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationWindowPattern::WaitForInputIdle


## -description


Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first. 


## -parameters




### -param milliseconds [in]

Type: <b>int</b>

The amount of time, in milliseconds, to wait for the associated process to become idle. 


### -param success [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Receives the result: <b>TRUE</b> if the window has entered the idle state, or <b>FALSE</b> if the time-out occurred.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/251fefdf-48c7-444a-89fc-fb27b10dcb0a">IUIAutomationWindowPattern</a>
 

 

