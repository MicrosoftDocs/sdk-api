---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.NormalizeElementBuildCache
title: IUIAutomationTreeWalker::NormalizeElementBuildCache (uiautomationclient.h)
description: Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["IUIAutomationTreeWalker interface [Windows Accessibility]","NormalizeElementBuildCache method","IUIAutomationTreeWalker.NormalizeElementBuildCache","IUIAutomationTreeWalker::NormalizeElementBuildCache","NormalizeElementBuildCache","NormalizeElementBuildCache method [Windows Accessibility]","NormalizeElementBuildCache method [Windows Accessibility]","IUIAutomationTreeWalker interface","uiauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache","uiauto_IUIAutomationTreeWalker_NormalizeBuildCache","uiautomationclient/IUIAutomationTreeWalker::NormalizeElementBuildCache","winauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache"]
old-location: winauto\uiauto_IUIAutomationTreeWalker_NormalizeBuildCache.htm
tech.root: WinAuto
ms.assetid: 62306545-1c5f-48ab-87c3-35bb6c3d94fa
ms.date: 12/05/2018
ms.keywords: IUIAutomationTreeWalker interface [Windows Accessibility],NormalizeElementBuildCache method, IUIAutomationTreeWalker.NormalizeElementBuildCache, IUIAutomationTreeWalker::NormalizeElementBuildCache, NormalizeElementBuildCache, NormalizeElementBuildCache method [Windows Accessibility], NormalizeElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, uiauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache, uiauto_IUIAutomationTreeWalker_NormalizeBuildCache, uiautomationclient/IUIAutomationTreeWalker::NormalizeElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache
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
 - IUIAutomationTreeWalker::NormalizeElementBuildCache
 - uiautomationclient/IUIAutomationTreeWalker::NormalizeElementBuildCache
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
 - IUIAutomationTreeWalker.NormalizeElementBuildCache
---

# IUIAutomationTreeWalker::NormalizeElementBuildCache


## -description

Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element from which to start the normalization.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the properties and control patterns to cache on the returned element.

### -param normalized [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the ancestor element nearest to the specified element in the tree view.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The element is normalized by navigating up the ancestor chain in the tree until an element that satisfies the view condition (specified by a previous call to <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-get_condition">IUIAutomationTreeWalker::Condition</a>) is reached. If the root element is reached, the root element is returned, even if it does not satisfy the view condition. 
            

This method is useful for applications that obtain references to UI Automation elements by hit-testing. The application might want to work only with specific types of elements, and can use <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement">IUIAutomationTreeWalker::NormalizeElement</a> to make sure that no matter what element is initially retrieved (for example, when a scroll bar gets the input focus), only the element of interest (such as a content element) is ultimately retrieved.