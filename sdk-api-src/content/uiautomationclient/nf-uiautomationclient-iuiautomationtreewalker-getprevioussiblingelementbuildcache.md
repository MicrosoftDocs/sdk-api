---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetPreviousSiblingElementBuildCache
title: IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache (uiautomationclient.h)
description: Retrieves the previous sibling element of the specified UI Automation element, and caches properties and control patterns.helpviewer_keywords: ["GetPreviousSiblingElementBuildCache","GetPreviousSiblingElementBuildCache method [Windows Accessibility]","GetPreviousSiblingElementBuildCache method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetPreviousSiblingElementBuildCache method","IUIAutomationTreeWalker.GetPreviousSiblingElementBuildCache","IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache","uiauto.uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache","uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache","uiautomationclient/IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache","winauto.uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache.htm
tech.root: WinAuto
ms.assetid: 09350915-0620-4c51-a4b5-25aa247d8241
ms.date: 12/05/2018
ms.keywords: GetPreviousSiblingElementBuildCache, GetPreviousSiblingElementBuildCache method [Windows Accessibility], GetPreviousSiblingElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetPreviousSiblingElementBuildCache method, IUIAutomationTreeWalker.GetPreviousSiblingElementBuildCache, IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache, uiauto.uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache, uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache, uiautomationclient/IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_GetPreviousSiblingBuildCache
f1_keywords:
- uiautomationclient/IUIAutomationTreeWalker.GetPreviousSiblingElementBuildCache
dev_langs:
- c++
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
- IUIAutomationTreeWalker.GetPreviousSiblingElementBuildCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTreeWalker::GetPreviousSiblingElementBuildCache


## -description


Retrieves the previous sibling element of the specified UI Automation element, and caches properties and control patterns.


## -parameters




### -param element [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the previous sibling.


### -param cacheRequest [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the properties and control patterns to cache on the returned element.


### -param previous [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the previous sibling element, or <b>NULL</b> if there is no sibling element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An element can have additional sibling elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the previous sibling element will be returned as the previous sibling on subsequent passes.



