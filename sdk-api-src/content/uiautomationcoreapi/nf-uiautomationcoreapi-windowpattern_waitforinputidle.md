---
UID: NF:uiautomationcoreapi.WindowPattern_WaitForInputIdle
title: WindowPattern_WaitForInputIdle function
author: windows-sdk-content
description: Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.
old-location: winauto\uiauto_WindowPattern_WaitForInputIdleConPat.htm
tech.root: WinAuto
ms.assetid: c2a319bd-9698-4671-b3d9-bcfd07c15aef
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WindowPattern_WaitForInputIdle, WindowPattern_WaitForInputIdle function [Windows Accessibility], uiauto.uiauto_WindowPattern_WaitForInputIdleConPat, uiauto_WindowPattern_WaitForInputIdleConPat, uiautomationcoreapi/WindowPattern_WaitForInputIdle, winauto.uiauto_WindowPattern_WaitForInputIdleConPat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - WindowPattern_WaitForInputIdle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WindowPattern_WaitForInputIdle function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param milliseconds [in]

Type: <b>int</b>

The number of milliseconds to wait before retrieving <i>pResult</i>.


### -param pResult [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the window is ready to accept user input; otherwise <b>FALSE</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



This method is typically used in conjunction with the handling of a WindowOpenedEvent 
        (<i>Window_WindowOpened_Event_GUID</i>).
        The implementation is dependent on the underlying application framework; 
        therefore this method may return some time after the window is ready for user input. 
        The calling code should not rely on this method to ascertain exactly when the window has become idle. 
        Use the value of <i>pResult</i> to determine if the window is ready for input or if the method timed out.





