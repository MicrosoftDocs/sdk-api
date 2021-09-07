---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetParentElement
title: IUIAutomationTreeWalker::GetParentElement (uiautomationclient.h)
description: Retrieves the parent element of the specified UI Automation element.
helpviewer_keywords: ["GetParentElement","GetParentElement method [Windows Accessibility]","GetParentElement method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetParentElement method","IUIAutomationTreeWalker.GetParentElement","IUIAutomationTreeWalker::GetParentElement","uiauto.uiauto_IUIAutomationTreeWalker_GetParent","uiauto_IUIAutomationTreeWalker_GetParent","uiautomationclient/IUIAutomationTreeWalker::GetParentElement","winauto.uiauto_IUIAutomationTreeWalker_GetParent"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetParent.htm
tech.root: WinAuto
ms.assetid: eaff4d83-a614-4559-a357-dc2d241ecf67
ms.date: 12/05/2018
ms.keywords: GetParentElement, GetParentElement method [Windows Accessibility], GetParentElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetParentElement method, IUIAutomationTreeWalker.GetParentElement, IUIAutomationTreeWalker::GetParentElement, uiauto.uiauto_IUIAutomationTreeWalker_GetParent, uiauto_IUIAutomationTreeWalker_GetParent, uiautomationclient/IUIAutomationTreeWalker::GetParentElement, winauto.uiauto_IUIAutomationTreeWalker_GetParent
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
 - IUIAutomationTreeWalker::GetParentElement
 - uiautomationclient/IUIAutomationTreeWalker::GetParentElement
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
 - IUIAutomationTreeWalker.GetParentElement
---

# IUIAutomationTreeWalker::GetParentElement


## -description

Retrieves the parent element of the specified UI Automation element.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the parent.

### -param parent [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the parent element, or <b>NULL</b> if there is no parent element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the  parent element will be returned as the parent on subsequent passes.