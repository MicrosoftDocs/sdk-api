---
UID: NF:uiautomationclient.IUIAutomation.ElementFromHandle
title: IUIAutomation::ElementFromHandle
author: windows-sdk-content
description: Retrieves a UI Automation element for the specified window.
old-location: winauto\uiauto_IUIAutomation_ElementFromHandle.htm
tech.root: WinAuto
ms.assetid: 07c6b7fa-80af-44c2-abcf-a167385892d5
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: ElementFromHandle, ElementFromHandle method [Windows Accessibility], ElementFromHandle method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromHandle method, IUIAutomation.ElementFromHandle, IUIAutomation::ElementFromHandle, uiauto.uiauto_IUIAutomation_ElementFromHandle, uiauto_IUIAutomation_ElementFromHandle, uiautomationclient/IUIAutomation::ElementFromHandle, winauto.uiauto_IUIAutomation_ElementFromHandle
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
 - IUIAutomation.ElementFromHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::ElementFromHandle


## -description


Retrieves a UI Automation element for the specified window.


## -parameters




### -param hwnd [in]

Type: <b>UIA_HWND</b>

The window handle.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/b6c1e03b-7c0e-4dee-b276-bfc7d6247d4e">IUIAutomation::ElementFromHandleBuildCache</a>
 

 

