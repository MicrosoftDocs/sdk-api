---
UID: NF:uiautomationclient.IUIAutomationElement7.FindAllWithOptionsBuildCache
title: IUIAutomationElement7::FindAllWithOptionsBuildCache
author: windows-sdk-content
description: Finds all matching elements in the specified order, but also caches their properties and patterns.
old-location: winauto\uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache.htm
old-project: WinAuto
ms.assetid: 92F9E34B-BFB9-48EA-A0EC-6E69EFB6307B
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FindAllWithOptionsBuildCache, FindAllWithOptionsBuildCache method [Windows Accessibility], FindAllWithOptionsBuildCache method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindAllWithOptionsBuildCache method, IUIAutomationElement7.FindAllWithOptionsBuildCache, IUIAutomationElement7::FindAllWithOptionsBuildCache, uiautomationclient/IUIAutomationElement7::FindAllWithOptionsBuildCache, winauto.uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache, winauto.uiauto_iuiautomationelement_findallwithoptionsbuildcache
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement7.FindAllWithOptionsBuildCache
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement7::FindAllWithOptionsBuildCache


## -description


Finds all matching elements in the specified order, but also caches their properties and patterns.


## -parameters




### -param scope




### -param condition [in]

A pointer to a condition that represents the criteria to match.


### -param cacheRequest [in]

A pointer to a cache request that specifies the control patterns and properties to include in the cache.


### -param traversalOptions

Enumeration value specifying the tree navigation order.


### -param root [in, optional]

A pointer to the element with which to begin the search.


### -param found






#### - foundElementsArray [out]

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found. 


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62B3D170-C3B3-48B8-92F8-3DF02F5D4082">IUIAutomationElement7</a>
 

 

