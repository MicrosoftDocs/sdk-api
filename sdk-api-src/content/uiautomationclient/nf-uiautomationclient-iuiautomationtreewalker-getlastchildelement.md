---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetLastChildElement
title: IUIAutomationTreeWalker::GetLastChildElement (uiautomationclient.h)
description: Retrieves the last child element of the specified UI Automation element.
helpviewer_keywords: ["GetLastChildElement","GetLastChildElement method [Windows Accessibility]","GetLastChildElement method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetLastChildElement method","IUIAutomationTreeWalker.GetLastChildElement","IUIAutomationTreeWalker::GetLastChildElement","uiauto.uiauto_IUIAutomationTreeWalker_GetLastChild","uiauto_IUIAutomationTreeWalker_GetLastChild","uiautomationclient/IUIAutomationTreeWalker::GetLastChildElement","winauto.uiauto_IUIAutomationTreeWalker_GetLastChild"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetLastChild.htm
tech.root: WinAuto
ms.assetid: 9e59d8f6-1540-4077-9e0e-f75bf8846da9
ms.date: 12/05/2018
ms.keywords: GetLastChildElement, GetLastChildElement method [Windows Accessibility], GetLastChildElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetLastChildElement method, IUIAutomationTreeWalker.GetLastChildElement, IUIAutomationTreeWalker::GetLastChildElement, uiauto.uiauto_IUIAutomationTreeWalker_GetLastChild, uiauto_IUIAutomationTreeWalker_GetLastChild, uiautomationclient/IUIAutomationTreeWalker::GetLastChildElement, winauto.uiauto_IUIAutomationTreeWalker_GetLastChild
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
 - IUIAutomationTreeWalker::GetLastChildElement
 - uiautomationclient/IUIAutomationTreeWalker::GetLastChildElement
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
 - IUIAutomationTreeWalker.GetLastChildElement
---

# IUIAutomationTreeWalker::GetLastChildElement


## -description

Retrieves the last child element of the specified UI Automation element.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to  the element for which to retrieve the last child.

### -param last [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the last child element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An element can have additional child elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the last child element will be returned as the last child on subsequent passes.