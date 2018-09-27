---
UID: NF:uiautomationclient.IUIAutomation.GetRootElementBuildCache
title: IUIAutomation::GetRootElementBuildCache
author: windows-sdk-content
description: Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
old-location: winauto\uiauto_IUIAutomation_GetRootElementBuildCache.htm
tech.root: WinAuto
ms.assetid: 0d2c0592-d29a-4e70-978e-55690aed82cb
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetRootElementBuildCache, GetRootElementBuildCache method [Windows Accessibility], GetRootElementBuildCache method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetRootElementBuildCache method, IUIAutomation.GetRootElementBuildCache, IUIAutomation::GetRootElementBuildCache, uiauto.uiauto_IUIAutomation_GetRootElementBuildCache, uiauto_IUIAutomation_GetRootElementBuildCache, uiautomationclient/IUIAutomation::GetRootElementBuildCache, winauto.uiauto_IUIAutomation_GetRootElementBuildCache
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
 - IUIAutomation.GetRootElementBuildCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::GetRootElementBuildCache


## -description


Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to the cache request, which specifies the properties and control patterns to store in the cache.


### -param root [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the root element as a starting point for finding other elements, using the <a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a> and <a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a> methods.

When searching from the root element, be sure to specify <a href="https://msdn.microsoft.com/en-us/library/Ee671699(v=VS.85).aspx">TreeScope_Children</a> in the scope of the search, not <a href="https://msdn.microsoft.com/en-us/library/Ee671699(v=VS.85).aspx">TreeScope_Descendants</a>. A search through the entire subtree of the desktop could iterate through thousands of items and lead to a stack overflow.

			




## -see-also




<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/9b6f3a78-a957-4ebd-a026-a8edb30faa88">IUIAutomation::GetRootElement</a>
 

 

