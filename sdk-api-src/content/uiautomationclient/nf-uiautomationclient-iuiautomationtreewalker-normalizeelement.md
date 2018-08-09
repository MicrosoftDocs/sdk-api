---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.NormalizeElement
title: IUIAutomationTreeWalker::NormalizeElement
author: windows-sdk-content
description: Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view.
old-location: winauto\uiauto_IUIAutomationTreeWalker_Normalize.htm
old-project: WinAuto
ms.assetid: 62616711-a841-4273-8e38-0d2344659d03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUIAutomationTreeWalker interface [Windows Accessibility],NormalizeElement method, IUIAutomationTreeWalker.NormalizeElement, IUIAutomationTreeWalker::NormalizeElement, NormalizeElement, NormalizeElement method [Windows Accessibility], NormalizeElement method [Windows Accessibility],IUIAutomationTreeWalker interface, uiauto.uiauto_IUIAutomationTreeWalker_Normalize, uiauto_IUIAutomationTreeWalker_Normalize, uiautomationclient/IUIAutomationTreeWalker::NormalizeElement, winauto.uiauto_IUIAutomationTreeWalker_Normalize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTreeWalker.NormalizeElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTreeWalker::NormalizeElement


## -description


Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view. 


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element from which to start the normalization.


### -param normalized [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the ancestor element nearest to the specified element in the tree view.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The element is normalized by navigating up the ancestor chain in the tree until an element that satisfies the view condition (specified by a previous call to <a href="https://msdn.microsoft.com/e62989ac-6fcf-4648-9b81-40b508ceae71">IUIAutomationTreeWalker::Condition</a>) is reached. But first, the passed element is tested to see if it matches a normalization condition. If so, the passed element is returned, even though it is not an ancestor.

 The method returns <b>UIA_E_ELEMENTNOTAVAILABLE</b> if no matching element has been found.

This method is useful for applications that obtain references to UI Automation elements by hit-testing. The application might want to work only with specific types of elements, and can use <b>IUIAutomationTreeWalker::Normalize</b> to make sure that no matter what element is initially retrieved (for example, when a scroll bar gets the input focus), only the element of interest (such as a content element) is ultimately retrieved. 
            



