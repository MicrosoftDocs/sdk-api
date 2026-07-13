---
UID: NF:uiautomationclient.IUIAutomation.ElementFromPointBuildCache
title: IUIAutomation::ElementFromPointBuildCache (uiautomationclient.h)
description: Retrieves the UI Automation element at the specified point on the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
helpviewer_keywords: ["ElementFromPointBuildCache","ElementFromPointBuildCache method [Windows Accessibility]","ElementFromPointBuildCache method [Windows Accessibility]","IUIAutomation interface","IUIAutomation interface [Windows Accessibility]","ElementFromPointBuildCache method","IUIAutomation.ElementFromPointBuildCache","IUIAutomation::ElementFromPointBuildCache","uiauto.uiauto_IUIAutomation_ElementFromPointBuildCache","uiauto_IUIAutomation_ElementFromPointBuildCache","uiautomationclient/IUIAutomation::ElementFromPointBuildCache","winauto.uiauto_IUIAutomation_ElementFromPointBuildCache"]
old-location: winauto\uiauto_IUIAutomation_ElementFromPointBuildCache.htm
tech.root: WinAuto
ms.assetid: fb3a8773-270a-4e33-bcbe-bde7794ea4ad
ms.date: 12/05/2018
ms.keywords: ElementFromPointBuildCache, ElementFromPointBuildCache method [Windows Accessibility], ElementFromPointBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromPointBuildCache method, IUIAutomation.ElementFromPointBuildCache, IUIAutomation::ElementFromPointBuildCache, uiauto.uiauto_IUIAutomation_ElementFromPointBuildCache, uiauto_IUIAutomation_ElementFromPointBuildCache, uiautomationclient/IUIAutomation::ElementFromPointBuildCache, winauto.uiauto_IUIAutomation_ElementFromPointBuildCache
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
 - IUIAutomation::ElementFromPointBuildCache
 - uiautomationclient/IUIAutomation::ElementFromPointBuildCache
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
 - IUIAutomation.ElementFromPointBuildCache
---

# IUIAutomation::ElementFromPointBuildCache


## -description

Retrieves the UI Automation element at the specified point on the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

## -parameters

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The desktop coordinates of the UI Automation element.

### -param cacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfrompoint">IUIAutomation::ElementFromPoint</a>