---
UID: NF:uiautomationclient.IUIAutomationTextRange3.GetEnclosingElementBuildCache
title: IUIAutomationTextRange3::GetEnclosingElementBuildCache
author: windows-sdk-content
description: Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call. This is equivalent to calling GetEnclosingElement, but adds the standard build cache pattern.
old-location: winauto\uiauto_IUIAutomationTextRange3_GetEnclosingElementBuildCache.htm
tech.root: WinAuto
ms.assetid: 6F5BC5DB-F9C0-40DF-8E29-FFACFBCAD80F
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetEnclosingElementBuildCache, GetEnclosingElementBuildCache method [Windows Accessibility], GetEnclosingElementBuildCache method [Windows Accessibility],IUIAutomationTextRange3 interface, IUIAutomationTextRange3 interface [Windows Accessibility],GetEnclosingElementBuildCache method, IUIAutomationTextRange3.GetEnclosingElementBuildCache, IUIAutomationTextRange3::GetEnclosingElementBuildCache, uiautomationclient/IUIAutomationTextRange3::GetEnclosingElementBuildCache, winauto.uiauto_IUIAutomationTextRange3_GetEnclosingElementBuildCache
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IUIAutomationTextRange3.GetEnclosingElementBuildCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomationTextRange3.GetEnclosingElementBuildCache
: 
---

# IUIAutomationTextRange3::GetEnclosingElementBuildCache


## -description


Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/0120b4af-6f08-4bbd-b649-0f8e84cda3b9">GetEnclosingElement</a>, but adds the standard build cache pattern.


## -parameters




### -param cacheRequest [in]

An <a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a> specifying the properties and control patterns to be cached.


### -param enclosingElement [out, retval]

Returns the enclosing element (and properties/patterns) of the text range if it meets the criteria of the supplied <i>cacheRequest</i>.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -remarks



Following the design of <a href="https://msdn.microsoft.com/0120b4af-6f08-4bbd-b649-0f8e84cda3b9">GetEnclosingElement</a>:

<ul>
<li>Gets the all-inclusive, innermost enclosing element of a text range and the supplied properties of the element.</li>
</ul>
As a result of a successful call, UI Automation clients are able call "Cached" APIs of <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> that are provided in the <i>cacheRequest</i>, for example, <a href="https://msdn.microsoft.com/3cd093fe-04ee-4b09-b5e7-28dad984951e">IUIAutomationElement::GetCachedPropertyValue</a>.




## -see-also




<a href="https://msdn.microsoft.com/3491996E-89EF-496D-94B6-FF8D121D3828">IUIAutomationTextRange3</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

