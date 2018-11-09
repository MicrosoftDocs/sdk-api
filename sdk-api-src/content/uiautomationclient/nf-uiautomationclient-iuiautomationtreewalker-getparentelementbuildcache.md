---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetParentElementBuildCache
title: IUIAutomationTreeWalker::GetParentElementBuildCache
author: windows-sdk-content
description: Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetParentBuildCache.htm
tech.root: WinAuto
ms.assetid: 1a1d9805-bcd7-4c5d-ac61-138ac75a523e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetParentElementBuildCache, GetParentElementBuildCache method [Windows Accessibility], GetParentElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetParentElementBuildCache method, IUIAutomationTreeWalker.GetParentElementBuildCache, IUIAutomationTreeWalker::GetParentElementBuildCache, uiauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache, uiauto_IUIAutomationTreeWalker_GetParentBuildCache, uiautomationclient/IUIAutomationTreeWalker::GetParentElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_GetParentBuildCache
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
 - IUIAutomationTreeWalker.GetParentElementBuildCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTreeWalker::GetParentElementBuildCache


## -description


Retrieves the parent element of the specified UI Automation element, and caches properties and control patterns.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the parent.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the properties and control patterns to cache on the returned element.


### -param parent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the parent element, or <b>NULL</b> if there is no parent element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the  parent element will be returned as the parent on subsequent passes.



