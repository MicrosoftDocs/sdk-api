---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.NormalizeElementBuildCache
title: IUIAutomationTreeWalker::NormalizeElementBuildCache
author: windows-sdk-content
description: Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.
old-location: winauto\uiauto_IUIAutomationTreeWalker_NormalizeBuildCache.htm
old-project: WinAuto
ms.assetid: 62306545-1c5f-48ab-87c3-35bb6c3d94fa
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationTreeWalker interface [Windows Accessibility],NormalizeElementBuildCache method, IUIAutomationTreeWalker.NormalizeElementBuildCache, IUIAutomationTreeWalker::NormalizeElementBuildCache, NormalizeElementBuildCache, NormalizeElementBuildCache method [Windows Accessibility], NormalizeElementBuildCache method [Windows Accessibility],IUIAutomationTreeWalker interface, uiauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache, uiauto_IUIAutomationTreeWalker_NormalizeBuildCache, uiautomationclient/IUIAutomationTreeWalker::NormalizeElementBuildCache, winauto.uiauto_IUIAutomationTreeWalker_NormalizeBuildCache
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationTreeWalker.NormalizeElementBuildCache
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTreeWalker::NormalizeElementBuildCache


## -description


Retrieves the ancestor element nearest to the specified Microsoft UI Automation element in the tree view, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element from which to start the normalization.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request that specifies the properties and control patterns to cache on the returned element.


### -param normalized [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the ancestor element nearest to the specified element in the tree view.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The element is normalized by navigating up the ancestor chain in the tree until an element that satisfies the view condition (specified by a previous call to <a href="https://msdn.microsoft.com/e62989ac-6fcf-4648-9b81-40b508ceae71">IUIAutomationTreeWalker::Condition</a>) is reached. If the root element is reached, the root element is returned, even if it does not satisfy the view condition. 
            

This method is useful for applications that obtain references to UI Automation elements by hit-testing. The application might want to work only with specific types of elements, and can use <a href="https://msdn.microsoft.com/62616711-a841-4273-8e38-0d2344659d03">IUIAutomationTreeWalker::NormalizeElement</a> to make sure that no matter what element is initially retrieved (for example, when a scroll bar gets the input focus), only the element of interest (such as a content element) is ultimately retrieved. 
            



