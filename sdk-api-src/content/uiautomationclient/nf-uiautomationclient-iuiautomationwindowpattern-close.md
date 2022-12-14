---
UID: NF:uiautomationclient.IUIAutomationWindowPattern.Close
title: IUIAutomationWindowPattern::Close (uiautomationclient.h)
description: Closes the window.
helpviewer_keywords: ["Close","Close method [Windows Accessibility]","Close method [Windows Accessibility]","IUIAutomationWindowPattern interface","IUIAutomationWindowPattern interface [Windows Accessibility]","Close method","IUIAutomationWindowPattern.Close","IUIAutomationWindowPattern::Close","uiauto.uiauto_IUIAutomationWindowPattern_Close","uiauto_IUIAutomationWindowPattern_Close","uiautomationclient/IUIAutomationWindowPattern::Close","winauto.uiauto_IUIAutomationWindowPattern_Close"]
old-location: winauto\uiauto_IUIAutomationWindowPattern_Close.htm
tech.root: WinAuto
ms.assetid: 925484e2-6ad1-49ca-b2d4-a6436e7a3ddd
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Accessibility], Close method [Windows Accessibility],IUIAutomationWindowPattern interface, IUIAutomationWindowPattern interface [Windows Accessibility],Close method, IUIAutomationWindowPattern.Close, IUIAutomationWindowPattern::Close, uiauto.uiauto_IUIAutomationWindowPattern_Close, uiauto_IUIAutomationWindowPattern_Close, uiautomationclient/IUIAutomationWindowPattern::Close, winauto.uiauto_IUIAutomationWindowPattern_Close
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
 - IUIAutomationWindowPattern::Close
 - uiautomationclient/IUIAutomationWindowPattern::Close
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
 - IUIAutomationWindowPattern.Close
---

# IUIAutomationWindowPattern::Close


## -description

Closes the window.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When called on a split pane control, this method closes the pane and removes the associated split. This method may also close all other panes, depending on implementation.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationwindowpattern">IUIAutomationWindowPattern</a>
