---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.NormalizeElement
title: IUIAutomationTreeWalker::NormalizeElement (uiautomationclient.h)
description: Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view.
helpviewer_keywords: ["IUIAutomationTreeWalker interface [Windows Accessibility]","NormalizeElement method","IUIAutomationTreeWalker.NormalizeElement","IUIAutomationTreeWalker::NormalizeElement","NormalizeElement","NormalizeElement method [Windows Accessibility]","NormalizeElement method [Windows Accessibility]","IUIAutomationTreeWalker interface","uiauto.uiauto_IUIAutomationTreeWalker_Normalize","uiauto_IUIAutomationTreeWalker_Normalize","uiautomationclient/IUIAutomationTreeWalker::NormalizeElement","winauto.uiauto_IUIAutomationTreeWalker_Normalize"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_Normalize.htm
tech.root: WinAuto
ms.assetid: 62616711-a841-4273-8e38-0d2344659d03
ms.date: 12/05/2018
ms.keywords: IUIAutomationTreeWalker interface [Windows Accessibility],NormalizeElement method, IUIAutomationTreeWalker.NormalizeElement, IUIAutomationTreeWalker::NormalizeElement, NormalizeElement, NormalizeElement method [Windows Accessibility], NormalizeElement method [Windows Accessibility],IUIAutomationTreeWalker interface, uiauto.uiauto_IUIAutomationTreeWalker_Normalize, uiauto_IUIAutomationTreeWalker_Normalize, uiautomationclient/IUIAutomationTreeWalker::NormalizeElement, winauto.uiauto_IUIAutomationTreeWalker_Normalize
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
 - IUIAutomationTreeWalker::NormalizeElement
 - uiautomationclient/IUIAutomationTreeWalker::NormalizeElement
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
 - IUIAutomationTreeWalker.NormalizeElement
---

# IUIAutomationTreeWalker::NormalizeElement


## -description

Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element from which to start the normalization.

### -param normalized [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the ancestor element nearest to the specified element in the tree view.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The element is normalized by navigating up the ancestor chain in the tree until an element that satisfies the view condition (specified by a previous call to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-get_condition">IUIAutomationTreeWalker::Condition</a>) is reached. But first, the passed element is tested to see if it matches a normalization condition. If so, the passed element is returned, even though it is not an ancestor.

 The method returns <b>UIA_E_ELEMENTNOTAVAILABLE</b> if no matching element has been found.

This method is useful for applications that obtain references to UI Automation elements by hit-testing. The application might want to work only with specific types of elements, and can use <b>IUIAutomationTreeWalker::Normalize</b> to make sure that no matter what element is initially retrieved (for example, when a scroll bar gets the input focus), only the element of interest (such as a content element) is ultimately retrieved.