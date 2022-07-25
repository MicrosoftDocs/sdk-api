---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetPreviousSiblingElement
title: IUIAutomationTreeWalker::GetPreviousSiblingElement (uiautomationclient.h)
description: Retrieves the previous sibling element of the specified UI Automation element.
helpviewer_keywords: ["GetPreviousSiblingElement","GetPreviousSiblingElement method [Windows Accessibility]","GetPreviousSiblingElement method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetPreviousSiblingElement method","IUIAutomationTreeWalker.GetPreviousSiblingElement","IUIAutomationTreeWalker::GetPreviousSiblingElement","uiauto.uiauto_IUIAutomationTreeWalker_GetPreviousSibling","uiauto_IUIAutomationTreeWalker_GetPreviousSibling","uiautomationclient/IUIAutomationTreeWalker::GetPreviousSiblingElement","winauto.uiauto_IUIAutomationTreeWalker_GetPreviousSibling"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetPreviousSibling.htm
tech.root: WinAuto
ms.assetid: 6e05f421-d037-4d3b-908e-44ddd818a3f1
ms.date: 12/05/2018
ms.keywords: GetPreviousSiblingElement, GetPreviousSiblingElement method [Windows Accessibility], GetPreviousSiblingElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetPreviousSiblingElement method, IUIAutomationTreeWalker.GetPreviousSiblingElement, IUIAutomationTreeWalker::GetPreviousSiblingElement, uiauto.uiauto_IUIAutomationTreeWalker_GetPreviousSibling, uiauto_IUIAutomationTreeWalker_GetPreviousSibling, uiautomationclient/IUIAutomationTreeWalker::GetPreviousSiblingElement, winauto.uiauto_IUIAutomationTreeWalker_GetPreviousSibling
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
 - IUIAutomationTreeWalker::GetPreviousSiblingElement
 - uiautomationclient/IUIAutomationTreeWalker::GetPreviousSiblingElement
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
 - IUIAutomationTreeWalker.GetPreviousSiblingElement
---

# IUIAutomationTreeWalker::GetPreviousSiblingElement


## -description

Retrieves the previous sibling element of the specified UI Automation element.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the previous sibling.

### -param previous [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the previous sibling element, or <b>NULL</b> if there is no sibling element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An element can have additional sibling elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the previous sibling element will be returned as the previous sibling on subsequent passes.