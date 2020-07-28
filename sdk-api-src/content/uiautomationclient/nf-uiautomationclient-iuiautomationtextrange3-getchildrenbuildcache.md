---
UID: NF:uiautomationclient.IUIAutomationTextRange3.GetChildrenBuildCache
title: IUIAutomationTextRange3::GetChildrenBuildCache (uiautomationclient.h)
description: Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call. This is equivalent to calling GetChildren, but adds the standard build cache pattern.
helpviewer_keywords: ["GetChildrenBuildCache","GetChildrenBuildCache method [Windows Accessibility]","GetChildrenBuildCache method [Windows Accessibility]","IUIAutomationTextRange3 interface","IUIAutomationTextRange3 interface [Windows Accessibility]","GetChildrenBuildCache method","IUIAutomationTextRange3.GetChildrenBuildCache","IUIAutomationTextRange3::GetChildrenBuildCache","uiautomationclient/IUIAutomationTextRange3::GetChildrenBuildCache","winauto.uiauto_IUIAutomationTextRange3_GetChildrenBuildCache"]
old-location: winauto\uiauto_IUIAutomationTextRange3_GetChildrenBuildCache.htm
tech.root: WinAuto
ms.assetid: 1C8F0E81-ED73-4752-BD27-7981508671D0
ms.date: 12/05/2018
ms.keywords: GetChildrenBuildCache, GetChildrenBuildCache method [Windows Accessibility], GetChildrenBuildCache method [Windows Accessibility],IUIAutomationTextRange3 interface, IUIAutomationTextRange3 interface [Windows Accessibility],GetChildrenBuildCache method, IUIAutomationTextRange3.GetChildrenBuildCache, IUIAutomationTextRange3::GetChildrenBuildCache, uiautomationclient/IUIAutomationTextRange3::GetChildrenBuildCache, winauto.uiauto_IUIAutomationTextRange3_GetChildrenBuildCache
f1_keywords:
- uiautomationclient/IUIAutomationTextRange3.GetChildrenBuildCache
dev_langs:
- c++
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
- IUIAutomationTextRange3.GetChildrenBuildCache
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextRange3::GetChildrenBuildCache


## -description


Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call.  This is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren">GetChildren</a>, but adds the standard build cache pattern.


## -parameters




### -param cacheRequest [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> specifying the properties and control patterns to be cached.


### -param children [out, retval]

Returns the children, and each child’s properties or patterns, of the text range that meet the criteria of the supplied <i>cacheRequest</i>.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -remarks



	Following the design of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren">GetChildren</a>:

<ul>
<li>Children that overlap with the text range, but are not entirely enclosed by it will also be included.</li>
<li>When no children exist, an empty collection is returned.</li>
</ul>
As a result of a successful call, UI Automation clients are able call "Cached" APIs of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> that are provided in the <i>cacheRequest</i>, for example, <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue">IUIAutomationElement::GetCachedPropertyValue</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange3">IUIAutomationTextRange3</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
 

 

