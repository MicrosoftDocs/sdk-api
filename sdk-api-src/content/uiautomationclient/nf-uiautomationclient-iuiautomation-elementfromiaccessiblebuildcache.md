---
UID: NF:uiautomationclient.IUIAutomation.ElementFromIAccessibleBuildCache
title: IUIAutomation::ElementFromIAccessibleBuildCache
author: windows-sdk-content
description: Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
old-location: winauto\uiauto_IUIAutomation_ElementFromIAccessibleBuildCache.htm
tech.root: WinAuto
ms.assetid: 7feadfc9-0be3-40ec-a986-526b207d1f38
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ElementFromIAccessibleBuildCache, ElementFromIAccessibleBuildCache method [Windows Accessibility], ElementFromIAccessibleBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],ElementFromIAccessibleBuildCache method, IUIAutomation.ElementFromIAccessibleBuildCache, IUIAutomation::ElementFromIAccessibleBuildCache, uiauto.uiauto_IUIAutomation_ElementFromIAccessibleBuildCache, uiauto_IUIAutomation_ElementFromIAccessibleBuildCache, uiautomationclient/IUIAutomation::ElementFromIAccessibleBuildCache, winauto.uiauto_IUIAutomation_ElementFromIAccessibleBuildCache
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
 - IUIAutomation.ElementFromIAccessibleBuildCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::ElementFromIAccessibleBuildCache


## -description


Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param accessible [in]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface of the accessible object.


### -param childId [in]

Type: <b>int</b>

The child ID of the accessible object.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>**</b>

The address of the cache request that specifies the properties and control patterns to store in the cache.


### -param element [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method enables Microsoft UI Automation clients to get <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interfaces for accessible objects implemented by a Microsoft Active Accessibility server. 

This method may fail if the server implements UI Automation provider interfaces alongside Microsoft Active Accessibility support. 

The method returns E_INVALIDARG if the underlying implementation of the UI Automation element is not a native Microsoft Active Accessibility server; that is, if a client attempts to retrieve the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface for an element originally supported by a proxy object from Oleacc.dll, or by the UIA-to-MSAA Bridge.




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/b6c1e03b-7c0e-4dee-b276-bfc7d6247d4e">IUIAutomation::ElementFromHandleBuildCache</a>
 

 

