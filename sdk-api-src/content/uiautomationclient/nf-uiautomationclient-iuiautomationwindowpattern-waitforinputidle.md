---
UID: NF:uiautomationclient.IUIAutomationWindowPattern.WaitForInputIdle
title: IUIAutomationWindowPattern::WaitForInputIdle (uiautomationclient.h)
description: Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first. (IUIAutomationWindowPattern.WaitForInputIdle)
helpviewer_keywords: ["IUIAutomationWindowPattern interface [Windows Accessibility]","WaitForInputIdle method","IUIAutomationWindowPattern.WaitForInputIdle","IUIAutomationWindowPattern::WaitForInputIdle","WaitForInputIdle","WaitForInputIdle method [Windows Accessibility]","WaitForInputIdle method [Windows Accessibility]","IUIAutomationWindowPattern interface","uiauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle","uiauto_IUIAutomationWindowPattern_WaitForInputIdle","uiautomationclient/IUIAutomationWindowPattern::WaitForInputIdle","winauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle"]
old-location: winauto\uiauto_IUIAutomationWindowPattern_WaitForInputIdle.htm
tech.root: WinAuto
ms.assetid: 2e08c3b1-6437-40ce-9dd3-2beb3e1f37fb
ms.date: 12/05/2018
ms.keywords: IUIAutomationWindowPattern interface [Windows Accessibility],WaitForInputIdle method, IUIAutomationWindowPattern.WaitForInputIdle, IUIAutomationWindowPattern::WaitForInputIdle, WaitForInputIdle, WaitForInputIdle method [Windows Accessibility], WaitForInputIdle method [Windows Accessibility],IUIAutomationWindowPattern interface, uiauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle, uiauto_IUIAutomationWindowPattern_WaitForInputIdle, uiautomationclient/IUIAutomationWindowPattern::WaitForInputIdle, winauto.uiauto_IUIAutomationWindowPattern_WaitForInputIdle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationWindowPattern::WaitForInputIdle
 - uiautomationclient/IUIAutomationWindowPattern::WaitForInputIdle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationWindowPattern.WaitForInputIdle
---

# IUIAutomationWindowPattern::WaitForInputIdle


## -description

Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.

## -parameters

### -param milliseconds [in]

Type: <b>int</b>

The amount of time, in milliseconds, to wait for the associated process to become idle.

### -param success [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives the result: <b>TRUE</b> if the window has entered the idle state, or <b>FALSE</b> if the time-out occurred.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationwindowpattern">IUIAutomationWindowPattern</a>
