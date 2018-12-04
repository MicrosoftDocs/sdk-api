---
UID: NF:uiautomationclient.IUIAutomation.GetFocusedElementBuildCache
title: IUIAutomation::GetFocusedElementBuildCache
author: windows-sdk-content
description: Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
old-location: winauto\uiauto_IUIAutomation_GetFocusedElementBuildCache.htm
tech.root: WinAuto
ms.assetid: c37c2703-ce01-44fe-a959-33b9f7d66e98
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetFocusedElementBuildCache, GetFocusedElementBuildCache method [Windows Accessibility], GetFocusedElementBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetFocusedElementBuildCache method, IUIAutomation.GetFocusedElementBuildCache, IUIAutomation::GetFocusedElementBuildCache, uiauto.uiauto_IUIAutomation_GetFocusedElementBuildCache, uiauto_IUIAutomation_GetFocusedElementBuildCache, uiautomationclient/IUIAutomation::GetFocusedElementBuildCache, winauto.uiauto_IUIAutomation_GetFocusedElementBuildCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IUIAutomation.GetFocusedElementBuildCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::GetFocusedElementBuildCache


## -description


Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



