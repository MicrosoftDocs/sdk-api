---
UID: NF:uiautomationclient.IUIAutomationElement7.FindAllWithOptionsBuildCache
title: IUIAutomationElement7::FindAllWithOptionsBuildCache (uiautomationclient.h)
author: windows-sdk-content
description: Finds all matching elements in the specified order, but also caches their properties and patterns.
old-location: winauto\uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache.htm
tech.root: WinAuto
ms.assetid: 92F9E34B-BFB9-48EA-A0EC-6E69EFB6307B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindAllWithOptionsBuildCache, FindAllWithOptionsBuildCache method [Windows Accessibility], FindAllWithOptionsBuildCache method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],FindAllWithOptionsBuildCache method, IUIAutomationElement7.FindAllWithOptionsBuildCache, IUIAutomationElement7::FindAllWithOptionsBuildCache, uiautomationclient/IUIAutomationElement7::FindAllWithOptionsBuildCache, winauto.uiauto_IUIAutomationElement7_FindAllWithOptionsBuildCache, winauto.uiauto_iuiautomationelement_findallwithoptionsbuildcache
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
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# IUIAutomationElement7::FindAllWithOptionsBuildCache


## -description


Finds all matching elements in the specified order, but also caches their properties and patterns.


## -parameters




### -param arg1 [in]

A pointer to a condition that represents the criteria to match.


### -param condition

TBD


### -param cacheRequest [in]

A pointer to a cache request that specifies the control patterns and properties to include in the cache.


### -param arg4 [in, optional]

A pointer to the element with which to begin the search.


### -param root

TBD


### -param found

TBD




#### - foundElementsArray [out]

Receives a pointer to an array of matching elements. Returns an empty array if no matching element is found. 


#### - traversalOptions

Enumeration value specifying the tree navigation order.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62B3D170-C3B3-48B8-92F8-3DF02F5D4082">IUIAutomationElement7</a>
 

 

