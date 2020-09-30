---
UID: NF:uiautomationclient.IUIAutomationElement7.FindAllWithOptionsBuildCache
title: IUIAutomationElement7::FindAllWithOptionsBuildCache (uiautomationclient.h)
description: Finds all matching elements in the specified order, but also caches their properties and patterns.
helpviewer_keywords: ["FindAllWithOptionsBuildCache","FindAllWithOptionsBuildCache method [Windows Accessibility]","FindAllWithOptionsBuildCache method [Windows Accessibility]","IUIAutomationElement7 interface","IUIAutomationElement7 interface [Windows Accessibility]","FindAllWithOptionsBuildCache method","IUIAutomationElement7.FindAllWithOptionsBuildCache","IUIAutomationElement7::FindAllWithOptionsBuildCache","uiautomationclient/IUIAutomationElement7::FindAllWithOptionsBuildCache","winauto.uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache","winauto.uiauto_iuiautomationelement_findallwithoptionsbuildcache"]
old-location: winauto\uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache.htm
tech.root: WinAuto
ms.assetid: 92F9E34B-BFB9-48EA-A0EC-6E69EFB6307B
ms.date: 12/05/2018
ms.keywords: FindAllWithOptionsBuildCache, FindAllWithOptionsBuildCache method [Windows Accessibility], FindAllWithOptionsBuildCache method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindAllWithOptionsBuildCache method, IUIAutomationElement7.FindAllWithOptionsBuildCache, IUIAutomationElement7::FindAllWithOptionsBuildCache, uiautomationclient/IUIAutomationElement7::FindAllWithOptionsBuildCache, winauto.uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache, winauto.uiauto_iuiautomationelement_findallwithoptionsbuildcache
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement7::FindAllWithOptionsBuildCache
 - uiautomationclient/IUIAutomationElement7::FindAllWithOptionsBuildCache
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
 - IUIAutomationElement7.FindAllWithOptionsBuildCache
---

# IUIAutomationElement7::FindAllWithOptionsBuildCache


## -description

Finds all matching elements in the specified order, but also caches their properties and patterns.

## -parameters

### -param scope [in]

Type: <b>[TreeScope](ne-uiautomationclient-treescope.md)</b>

The scope of the request.

When an element is retrieved, caching can be performed for only the element itself (the default behavior), or for the element and its children or descendants. This property describes the scope of the request.

### -param condition [in]

Type: <b>[IUIAutomationCondition](nn-uiautomationclient-iuiautomationcondition.md)</b>

The primary interface for conditions used in filtering when searching for elements in the UI Automation tree.

### -param cacheRequest [in]

Type: <b>[IUIAutomationCacheRequest](nn-uiautomationclient-iuiautomationcacherequest.md)</b>

A pointer to a cache request that specifies the control patterns and properties to include in the cache.

### -param traversalOptions [in]

Type: <b>[TreeTraversalOptions](ne-uiautomationclient-treetraversaloptions.md)</b>

The tree navigation order.

### -param root [in]

Type: <b>[IUIAutomationElement](nn-uiautomationclient-iuiautomationelement.md)</b>

A pointer to the element with which to begin the search.

### -param found [out, retval]

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement7">IUIAutomationElement7</a>