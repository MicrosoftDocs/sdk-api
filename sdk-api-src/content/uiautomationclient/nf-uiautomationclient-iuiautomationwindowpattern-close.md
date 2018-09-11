---
UID: NF:uiautomationclient.IUIAutomationWindowPattern.Close
title: IUIAutomationWindowPattern::Close
author: windows-sdk-content
description: Closes the window.
old-location: winauto\uiauto_IUIAutomationWindowPattern_Close.htm
tech.root: WinAuto
ms.assetid: 925484e2-6ad1-49ca-b2d4-a6436e7a3ddd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Close, Close method [Windows Accessibility], Close method [Windows Accessibility],IUIAutomationWindowPattern interface, IUIAutomationWindowPattern interface [Windows Accessibility],Close method, IUIAutomationWindowPattern.Close, IUIAutomationWindowPattern::Close, uiauto.uiauto_IUIAutomationWindowPattern_Close, uiauto_IUIAutomationWindowPattern_Close, uiautomationclient/IUIAutomationWindowPattern::Close, winauto.uiauto_IUIAutomationWindowPattern_Close
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
 - IUIAutomationWindowPattern.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationWindowPattern::Close


## -description


Closes the window.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When called on a split pane control, this method closes the pane and removes the associated split. This method may also close all other panes, depending on implementation.




## -see-also




<a href="https://msdn.microsoft.com/251fefdf-48c7-444a-89fc-fb27b10dcb0a">IUIAutomationWindowPattern</a>
 

 

