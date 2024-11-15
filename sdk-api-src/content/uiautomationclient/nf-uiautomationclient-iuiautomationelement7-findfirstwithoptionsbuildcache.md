---
UID: NF:uiautomationclient.IUIAutomationElement7.FindFirstWithOptionsBuildCache
title: IUIAutomationElement7::FindFirstWithOptionsBuildCache (uiautomationclient.h)
description: Finds the first matching element in the specified order, but also caches its properties and pattern.
helpviewer_keywords: ["FindFirstWithOptionsBuildCache","FindFirstWithOptionsBuildCache method [Windows Accessibility]","FindFirstWithOptionsBuildCache method [Windows Accessibility]","IUIAutomationElement7 interface","IUIAutomationElement7 interface [Windows Accessibility]","FindFirstWithOptionsBuildCache method","IUIAutomationElement7.FindFirstWithOptionsBuildCache","IUIAutomationElement7::FindFirstWithOptionsBuildCache","uiautomationclient/IUIAutomationElement7::FindFirstWithOptionsBuildCache","winauto.uiauto_IUIAutomationElement7_FindFirstWithOptionsBuildCache","winauto.uiauto_iuiautomationelement_findfirstwithoptionsbuildcache"]
old-location: winauto\uiauto_IUIAutomationElement7_FindFirstWithOptionsBuildCache.htm
tech.root: WinAuto
ms.assetid: 03683C11-7AB0-4933-A7C1-4A75A12079E1
ms.date: 12/05/2018
ms.keywords: FindFirstWithOptionsBuildCache, FindFirstWithOptionsBuildCache method [Windows Accessibility], FindFirstWithOptionsBuildCache method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindFirstWithOptionsBuildCache method, IUIAutomationElement7.FindFirstWithOptionsBuildCache, IUIAutomationElement7::FindFirstWithOptionsBuildCache, uiautomationclient/IUIAutomationElement7::FindFirstWithOptionsBuildCache, winauto.uiauto_IUIAutomationElement7_FindFirstWithOptionsBuildCache, winauto.uiauto_iuiautomationelement_findfirstwithoptionsbuildcache
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
 - IUIAutomationElement7::FindFirstWithOptionsBuildCache
 - uiautomationclient/IUIAutomationElement7::FindFirstWithOptionsBuildCache
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
 - IUIAutomationElement7.FindFirstWithOptionsBuildCache
---

# IUIAutomationElement7::FindFirstWithOptionsBuildCache


## -description

Finds the first matching element in the specified order, but also caches its properties and pattern.

## -parameters

### -param scope [in]

A combination of values specifying the scope of the search.

### -param condition [in]

A pointer to a condition that represents the criteria to match.

### -param cacheRequest [in]

A pointer to a cache request that specifies the control patterns and properties to include in the cache.

### -param traversalOptions

Enumeration value specifying the tree navigation order.

### -param root [in, optional]

A pointer to the element with which to begin the search.

### -param found [out, retval]

Receives a pointer to the element. <b>NULL</b> is returned if no matching element is found.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement7">IUIAutomationElement7</a>