---
UID: NF:uiautomationclient.IUIAutomation.GetFocusedElementBuildCache
title: IUIAutomation::GetFocusedElementBuildCache (uiautomationclient.h)
description: Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["GetFocusedElementBuildCache","GetFocusedElementBuildCache method [Windows Accessibility]","GetFocusedElementBuildCache method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","GetFocusedElementBuildCache method","IUIAutomation.GetFocusedElementBuildCache","IUIAutomation::GetFocusedElementBuildCache","uiauto.uiauto_IUIAutomation_GetFocusedElementBuildCache","uiauto_IUIAutomation_GetFocusedElementBuildCache","uiautomationclient/IUIAutomation::GetFocusedElementBuildCache","winauto.uiauto_IUIAutomation_GetFocusedElementBuildCache"]
old-location: winauto\uiauto_IUIAutomation_GetFocusedElementBuildCache.htm
tech.root: WinAuto
ms.assetid: c37c2703-ce01-44fe-a959-33b9f7d66e98
ms.date: 12/05/2018
ms.keywords: GetFocusedElementBuildCache, GetFocusedElementBuildCache method [Windows Accessibility], GetFocusedElementBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetFocusedElementBuildCache method, IUIAutomation.GetFocusedElementBuildCache, IUIAutomation::GetFocusedElementBuildCache, uiauto.uiauto_IUIAutomation_GetFocusedElementBuildCache, uiauto_IUIAutomation_GetFocusedElementBuildCache, uiautomationclient/IUIAutomation::GetFocusedElementBuildCache, winauto.uiauto_IUIAutomation_GetFocusedElementBuildCache
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
 - IUIAutomation::GetFocusedElementBuildCache
 - uiautomationclient/IUIAutomation::GetFocusedElementBuildCache
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
 - IUIAutomation.GetFocusedElementBuildCache
---

# IUIAutomation::GetFocusedElementBuildCache


## -description

Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

## -parameters

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.