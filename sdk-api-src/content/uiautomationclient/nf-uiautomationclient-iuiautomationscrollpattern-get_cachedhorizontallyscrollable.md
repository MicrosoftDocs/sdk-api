---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.get_CachedHorizontallyScrollable
title: IUIAutomationScrollPattern::get_CachedHorizontallyScrollable (uiautomationclient.h)
description: Retrieves a cached value that indicates whether the element can scroll horizontally.
helpviewer_keywords: ["CachedHorizontallyScrollable property [Windows Accessibility]","CachedHorizontallyScrollable property [Windows Accessibility]","IUIAutomationScrollPattern interface","IUIAutomationScrollPattern interface [Windows Accessibility]","CachedHorizontallyScrollable property","IUIAutomationScrollPattern.CachedHorizontallyScrollable","IUIAutomationScrollPattern.get_CachedHorizontallyScrollable","IUIAutomationScrollPattern::CachedHorizontallyScrollable","IUIAutomationScrollPattern::get_CachedHorizontallyScrollable","get_CachedHorizontallyScrollable","uiauto.uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable","uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable","uiautomationclient/IUIAutomationScrollPattern::CachedHorizontallyScrollable","uiautomationclient/IUIAutomationScrollPattern::get_CachedHorizontallyScrollable","winauto.uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable"]
old-location: winauto\uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable.htm
tech.root: WinAuto
ms.assetid: 9089e237-2115-47b6-a1eb-eaea5a93586e
ms.date: 12/05/2018
ms.keywords: CachedHorizontallyScrollable property [Windows Accessibility], CachedHorizontallyScrollable property [Windows Accessibility],IUIAutomationScrollPattern interface, IUIAutomationScrollPattern interface [Windows Accessibility],CachedHorizontallyScrollable property, IUIAutomationScrollPattern.CachedHorizontallyScrollable, IUIAutomationScrollPattern.get_CachedHorizontallyScrollable, IUIAutomationScrollPattern::CachedHorizontallyScrollable, IUIAutomationScrollPattern::get_CachedHorizontallyScrollable, get_CachedHorizontallyScrollable, uiauto.uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable, uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable, uiautomationclient/IUIAutomationScrollPattern::CachedHorizontallyScrollable, uiautomationclient/IUIAutomationScrollPattern::get_CachedHorizontallyScrollable, winauto.uiauto_IUIAutomationScrollPattern_CachedHorizontallyScrollable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationScrollPattern::get_CachedHorizontallyScrollable
 - uiautomationclient/IUIAutomationScrollPattern::get_CachedHorizontallyScrollable
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
 - IUIAutomationScrollPattern.CachedHorizontallyScrollable
 - IUIAutomationScrollPattern.get_CachedHorizontallyScrollable
---

# IUIAutomationScrollPattern::get_CachedHorizontallyScrollable


## -description

Retrieves a cached value that indicates whether the element can scroll horizontally.

This property is read-only.

## -parameters

## -remarks

This property can be dynamic. For example, the content area of the element might not be larger than the current viewable area, meaning that the property is <b>FALSE</b>. However, resizing the element or adding child items can increase the bounds of the content area beyond the viewable area, making the property <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationscrollpattern">IUIAutomationScrollPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationscrollpattern-get_cachedverticallyscrollable">IUIAutomationScrollPattern::CachedVerticallyScrollable</a>