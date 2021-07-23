---
UID: NF:uiautomationclient.IUIAutomation.ElementFromHandleBuildCache
title: IUIAutomation::ElementFromHandleBuildCache (uiautomationclient.h)
description: Retrieves a UI Automation element for the specified window, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["ElementFromHandleBuildCache","ElementFromHandleBuildCache method [Windows Accessibility]","ElementFromHandleBuildCache method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","ElementFromHandleBuildCache method","IUIAutomation.ElementFromHandleBuildCache","IUIAutomation::ElementFromHandleBuildCache","uiauto.uiauto_IUIAutomation_ElementFromHandleBuildCache","uiauto_IUIAutomation_ElementFromHandleBuildCache","uiautomationclient/IUIAutomation::ElementFromHandleBuildCache","winauto.uiauto_IUIAutomation_ElementFromHandleBuildCache"]
old-location: winauto\uiauto_IUIAutomation_ElementFromHandleBuildCache.htm
tech.root: WinAuto
ms.assetid: b6c1e03b-7c0e-4dee-b276-bfc7d6247d4e
ms.date: 12/05/2018
ms.keywords: ElementFromHandleBuildCache, ElementFromHandleBuildCache method [Windows Accessibility], ElementFromHandleBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromHandleBuildCache method, IUIAutomation.ElementFromHandleBuildCache, IUIAutomation::ElementFromHandleBuildCache, uiauto.uiauto_IUIAutomation_ElementFromHandleBuildCache, uiauto_IUIAutomation_ElementFromHandleBuildCache, uiautomationclient/IUIAutomation::ElementFromHandleBuildCache, winauto.uiauto_IUIAutomation_ElementFromHandleBuildCache
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
 - IUIAutomation::ElementFromHandleBuildCache
 - uiautomationclient/IUIAutomation::ElementFromHandleBuildCache
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
 - IUIAutomation.ElementFromHandleBuildCache
---

# IUIAutomation::ElementFromHandleBuildCache


## -description

Retrieves a UI Automation element for the specified window, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

## -parameters

### -param hwnd [in]

Type: <b>UIA_HWND</b>

The window handle.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromhandle">IUIAutomation::ElementFromHandle</a>