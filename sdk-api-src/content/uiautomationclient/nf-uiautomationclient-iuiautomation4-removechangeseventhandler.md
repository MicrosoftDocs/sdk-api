---
UID: NF:uiautomationclient.IUIAutomation4.RemoveChangesEventHandler
title: IUIAutomation4::RemoveChangesEventHandler
author: windows-sdk-content
description: Removes a changes event handler.
old-location: winauto\uiauto_IUIAutomation4_RemoveChangesEventHandler.htm
tech.root: WinAuto
ms.assetid: 18F65528-3038-4FF7-AEB8-AAEA3A5BB058
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IUIAutomation4 interface [Windows Accessibility],RemoveChangesEventHandler method, IUIAutomation4.RemoveChangesEventHandler, IUIAutomation4::RemoveChangesEventHandler, RemoveChangesEventHandler, RemoveChangesEventHandler method [Windows Accessibility], RemoveChangesEventHandler method [Windows Accessibility],IUIAutomation4 interface, uiautomationclient/IUIAutomation4::RemoveChangesEventHandler, winauto.uiauto_IUIAutomation4_RemoveChangesEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IUIAutomation4.RemoveChangesEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation4::RemoveChangesEventHandler


## -description


Removes a changes event handler.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/8DCF8826-B688-416C-9195-34E0290054AA">IUIAutomationChangesEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="https://msdn.microsoft.com/E479ACCA-9372-463F-A992-8030E33A2341">AddChangesEventHandler</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CA616076-CD04-4753-9605-093C9529C826">IUIAutomation4</a>
 

 

