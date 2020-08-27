---
UID: NF:uiautomationclient.IUIAutomation4.RemoveChangesEventHandler
title: IUIAutomation4::RemoveChangesEventHandler (uiautomationclient.h)
description: Removes a changes event handler.
helpviewer_keywords: ["IUIAutomation4 interface [Windows Accessibility]","RemoveChangesEventHandler method","IUIAutomation4.RemoveChangesEventHandler","IUIAutomation4::RemoveChangesEventHandler","RemoveChangesEventHandler","RemoveChangesEventHandler method [Windows Accessibility]","RemoveChangesEventHandler method [Windows Accessibility]","IUIAutomation4 interface","uiautomationclient/IUIAutomation4::RemoveChangesEventHandler","winauto.uiauto_IUIAutomation4_RemoveChangesEventHandler"]
old-location: winauto\uiauto_IUIAutomation4_RemoveChangesEventHandler.htm
tech.root: WinAuto
ms.assetid: 18F65528-3038-4FF7-AEB8-AAEA3A5BB058
ms.date: 12/05/2018
ms.keywords: IUIAutomation4 interface [Windows Accessibility],RemoveChangesEventHandler method, IUIAutomation4.RemoveChangesEventHandler, IUIAutomation4::RemoveChangesEventHandler, RemoveChangesEventHandler, RemoveChangesEventHandler method [Windows Accessibility], RemoveChangesEventHandler method [Windows Accessibility],IUIAutomation4 interface, uiautomationclient/IUIAutomation4::RemoveChangesEventHandler, winauto.uiauto_IUIAutomation4_RemoveChangesEventHandler
f1_keywords:
- uiautomationclient/IUIAutomation4.RemoveChangesEventHandler
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation4::RemoveChangesEventHandler


## -description


Removes a changes event handler.


## -parameters




### -param element [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element from which to remove the handler.


### -param handler [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationchangeseventhandler">IUIAutomationChangesEventHandler</a>*</b>

A pointer to the  interface that was passed to <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation4-addchangeseventhandler">AddChangesEventHandler</a>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation4">IUIAutomation4</a>
 

 

