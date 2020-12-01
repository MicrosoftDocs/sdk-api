---
UID: NF:uiautomationclient.IUIAutomationTextRange3.GetEnclosingElementBuildCache
title: IUIAutomationTextRange3::GetEnclosingElementBuildCache (uiautomationclient.h)
description: Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call. This is equivalent to calling GetEnclosingElement, but adds the standard build cache pattern.
helpviewer_keywords: ["GetEnclosingElementBuildCache","GetEnclosingElementBuildCache method [Windows Accessibility]","GetEnclosingElementBuildCache method [Windows Accessibility]","IUIAutomationTextRange3 interface","IUIAutomationTextRange3 interface [Windows Accessibility]","GetEnclosingElementBuildCache method","IUIAutomationTextRange3.GetEnclosingElementBuildCache","IUIAutomationTextRange3::GetEnclosingElementBuildCache","uiautomationclient/IUIAutomationTextRange3::GetEnclosingElementBuildCache","winauto.uiauto_IUIAutomationTextRange3_GetEnclosingElementBuildCache"]
old-location: winauto\uiauto_IUIAutomationTextRange3_GetEnclosingElementBuildCache.htm
tech.root: WinAuto
ms.assetid: 6F5BC5DB-F9C0-40DF-8E29-FFACFBCAD80F
ms.date: 12/05/2018
ms.keywords: GetEnclosingElementBuildCache, GetEnclosingElementBuildCache method [Windows Accessibility], GetEnclosingElementBuildCache method [Windows Accessibility],IUIAutomationTextRange3 interface, IUIAutomationTextRange3 interface [Windows Accessibility],GetEnclosingElementBuildCache method, IUIAutomationTextRange3.GetEnclosingElementBuildCache, IUIAutomationTextRange3::GetEnclosingElementBuildCache, uiautomationclient/IUIAutomationTextRange3::GetEnclosingElementBuildCache, winauto.uiauto_IUIAutomationTextRange3_GetEnclosingElementBuildCache
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTextRange3::GetEnclosingElementBuildCache
 - uiautomationclient/IUIAutomationTextRange3::GetEnclosingElementBuildCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange3.GetEnclosingElementBuildCache
---

# IUIAutomationTextRange3::GetEnclosingElementBuildCache


## -description

Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call.  This is equivalent to calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement">GetEnclosingElement</a>, but adds the standard build cache pattern.

## -parameters

### -param cacheRequest [in]

An <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a> specifying the properties and control patterns to be cached.

### -param enclosingElement [out, retval]

Returns the enclosing element (and properties/patterns) of the text range if it meets the criteria of the supplied <i>cacheRequest</i>.

## -returns

Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.

## -remarks

Following the design of <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement">GetEnclosingElement</a>:

<ul>
<li>Gets the all-inclusive, innermost enclosing element of a text range and the supplied properties of the element.</li>
</ul>
As a result of a successful call, UI Automation clients are able call "Cached" APIs of <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> that are provided in the <i>cacheRequest</i>, for example, <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue">IUIAutomationElement::GetCachedPropertyValue</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange3">IUIAutomationTextRange3</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>