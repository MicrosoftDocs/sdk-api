---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetFirstChildElementBuildCache
title: IUIAutomationTreeWalker::GetFirstChildElementBuildCache (uiautomationclient.h)
description: Retrieves the first child element of the specified UI Automation element, and caches properties and control patterns.
helpviewer_keywords: ["GetFirstChildElementBuildCache","GetFirstChildElementBuildCache method [Windows Accessibility]","GetFirstChildElementBuildCache method [Windows Accessibility]","IUIAutomationTreeWalker interface","IUIAutomationTreeWalker interface [Windows Accessibility]","GetFirstChildElementBuildCache method","IUIAutomationTreeWalker.GetFirstChildElementBuildCache","IUIAutomationTreeWalker::GetFirstChildElementBuildCache","uiauto.uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache","uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache","uiautomationclient/IUIAutomationTreeWalker::GetFirstChildElementBuildCache","winauto.uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache.htm
tech.root: WinAuto
ms.assetid: 42bdc6c4-8ee5-4338-aba1-9740221786c8
ms.date: 12/05/2018
ms.keywords: GetFirstChildElementBuildCache, GetFirstChildElementBuildCache method [Windows Accessibility], GetFirstChildElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetFirstChildElementBuildCache method, IUIAutomationTreeWalker.GetFirstChildElementBuildCache, IUIAutomationTreeWalker::GetFirstChildElementBuildCache, uiauto.uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache, uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache, uiautomationclient/IUIAutomationTreeWalker::GetFirstChildElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_GetFirstChildBuildCache
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
 - IUIAutomationTreeWalker::GetFirstChildElementBuildCache
 - uiautomationclient/IUIAutomationTreeWalker::GetFirstChildElementBuildCache
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
 - IUIAutomationTreeWalker.GetFirstChildElementBuildCache
---

# IUIAutomationTreeWalker::GetFirstChildElementBuildCache


## -description

Retrieves the first child element of the specified UI Automation element, and caches properties and control patterns.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the first child.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to  a cache request that specifies the properties and control patterns to cache on the returned element.

### -param first [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the first child element, or <b>NULL</b> if there is no child element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An element can have additional child elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the first child element will be returned as the first child on subsequent passes.