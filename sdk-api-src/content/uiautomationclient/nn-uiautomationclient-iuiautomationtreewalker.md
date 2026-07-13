---
UID: NN:uiautomationclient.IUIAutomationTreeWalker
title: IUIAutomationTreeWalker (uiautomationclient.h)
description: Exposes properties and methods that UI Automation client applications use to view and navigate the UI Automation elements on the desktop.
helpviewer_keywords: ["IUIAutomationTreeWalker","IUIAutomationTreeWalker interface [Windows Accessibility]","IUIAutomationTreeWalker interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTreeWalker","uiauto_IUIAutomationTreeWalker","uiautomationclient/IUIAutomationTreeWalker","winauto.uiauto_IUIAutomationTreeWalker"]
old-location: winauto\uiauto_IUIAutomationTreeWalker.htm
tech.root: WinAuto
ms.assetid: adb4afed-63b9-42b4-8a8d-673d4813bb52
ms.date: 12/05/2018
ms.keywords: IUIAutomationTreeWalker, IUIAutomationTreeWalker interface [Windows Accessibility], IUIAutomationTreeWalker interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTreeWalker, uiauto_IUIAutomationTreeWalker, uiautomationclient/IUIAutomationTreeWalker, winauto.uiauto_IUIAutomationTreeWalker
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTreeWalker
 - uiautomationclient/IUIAutomationTreeWalker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTreeWalker
---

# IUIAutomationTreeWalker interface


## -description

Exposes properties and methods that UI Automation client applications use to view and navigate the UI Automation elements on the desktop.

## -inheritance

The <b>IUIAutomationTreeWalker</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTreeWalker</b> also has these types of members:

## -remarks

UI Automation clients view the elements on the desktop as a set of <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> objects arranged in a tree structure. Using the <b>IUIAutomationTreeWalker</b> interface, a client application can navigate by selecting a view of the tree and stepping from one element to another in a specified direction using methods such as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelement">GetFirstChildElement</a> and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-getnextsiblingelement">GetNextSiblingElement</a>.

Navigating the tree using <b>IUIAutomationTreeWalker</b> can result in cross-process calls and is not as efficient as locating an element using the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">IUIAutomationElement::FindAll</a> or <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">IUIAutomationElement::FindFirst</a> methods.

If your client application might try to find elements in its own user interface, you must make all UI Automation calls on a separate thread.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtreewalker">CreateTreeWalker</a>



<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
