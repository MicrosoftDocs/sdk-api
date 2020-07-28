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
f1_keywords:
- uiautomationclient/IUIAutomation.ElementFromPointBuildCache
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
- IUIAutomation.ElementFromPointBuildCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::ElementFromPointBuildCache


## -description


Retrieves the UI Automation element at the specified point on the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param pt [in]

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>

The desktop coordinates of the UI Automation element.


### -param cacheRequest [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.


### -param element [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfrompoint">IUIAutomation::ElementFromPoint</a>
 

 

