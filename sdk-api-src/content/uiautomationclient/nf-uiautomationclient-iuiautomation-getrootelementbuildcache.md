---
UID: NF:uiautomationclient.IUIAutomation.GetRootElementBuildCache
title: IUIAutomation::GetRootElementBuildCache (uiautomationclient.h)
description: Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["GetRootElementBuildCache","GetRootElementBuildCache method [Windows Accessibility]","GetRootElementBuildCache method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","GetRootElementBuildCache method","IUIAutomation.GetRootElementBuildCache","IUIAutomation::GetRootElementBuildCache","uiauto.uiauto_IUIAutomation_GetRootElementBuildCache","uiauto_IUIAutomation_GetRootElementBuildCache","uiautomationclient/IUIAutomation::GetRootElementBuildCache","winauto.uiauto_IUIAutomation_GetRootElementBuildCache"]
old-location: winauto\uiauto_IUIAutomation_GetRootElementBuildCache.htm
tech.root: WinAuto
ms.assetid: 0d2c0592-d29a-4e70-978e-55690aed82cb
ms.date: 12/05/2018
ms.keywords: GetRootElementBuildCache, GetRootElementBuildCache method [Windows Accessibility], GetRootElementBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetRootElementBuildCache method, IUIAutomation.GetRootElementBuildCache, IUIAutomation::GetRootElementBuildCache, uiauto.uiauto_IUIAutomation_GetRootElementBuildCache, uiauto_IUIAutomation_GetRootElementBuildCache, uiautomationclient/IUIAutomation::GetRootElementBuildCache, winauto.uiauto_IUIAutomation_GetRootElementBuildCache
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
 - IUIAutomation::GetRootElementBuildCache
 - uiautomationclient/IUIAutomation::GetRootElementBuildCache
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
 - IUIAutomation.GetRootElementBuildCache
---

# IUIAutomation::GetRootElementBuildCache


## -description

Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

## -parameters

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.

### -param root [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can use the root element as a starting point for finding other elements, using the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a> and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a> methods.

When searching from the root element, be sure to specify <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Children</a> in the scope of the search, not <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getrootelement">IUIAutomation::GetRootElement</a>