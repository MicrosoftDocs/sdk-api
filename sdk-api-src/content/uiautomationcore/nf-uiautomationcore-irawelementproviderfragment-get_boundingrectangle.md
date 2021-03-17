---
UID: NF:uiautomationcore.IRawElementProviderFragment.get_BoundingRectangle
title: IRawElementProviderFragment::get_BoundingRectangle (uiautomationcore.h)
description: Specifies the bounding rectangle of this element.
helpviewer_keywords: ["BoundingRectangle property [Windows Accessibility]","BoundingRectangle property [Windows Accessibility]","IRawElementProviderFragment interface","IRawElementProviderFragment interface [Windows Accessibility]","BoundingRectangle property","IRawElementProviderFragment.BoundingRectangle","IRawElementProviderFragment.get_BoundingRectangle","IRawElementProviderFragment::BoundingRectangle","IRawElementProviderFragment::get_BoundingRectangle","get_BoundingRectangle","uiauto.uiauto_IRawElementProviderFragment_BoundingRectangle","uiauto_IRawElementProviderFragment_BoundingRectangle","uiautomationcore/IRawElementProviderFragment::BoundingRectangle","uiautomationcore/IRawElementProviderFragment::get_BoundingRectangle","winauto.uiauto_IRawElementProviderFragment_BoundingRectangle"]
old-location: winauto\uiauto_IRawElementProviderFragment_BoundingRectangle.htm
tech.root: WinAuto
ms.assetid: 443df4af-06cd-4866-bdeb-b1770ccb9060
ms.date: 12/05/2018
ms.keywords: BoundingRectangle property [Windows Accessibility], BoundingRectangle property [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],BoundingRectangle property, IRawElementProviderFragment.BoundingRectangle, IRawElementProviderFragment.get_BoundingRectangle, IRawElementProviderFragment::BoundingRectangle, IRawElementProviderFragment::get_BoundingRectangle, get_BoundingRectangle, uiauto.uiauto_IRawElementProviderFragment_BoundingRectangle, uiauto_IRawElementProviderFragment_BoundingRectangle, uiautomationcore/IRawElementProviderFragment::BoundingRectangle, uiautomationcore/IRawElementProviderFragment::get_BoundingRectangle, winauto.uiauto_IRawElementProviderFragment_BoundingRectangle
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - IRawElementProviderFragment::get_BoundingRectangle
 - uiautomationcore/IRawElementProviderFragment::get_BoundingRectangle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderFragment.BoundingRectangle
 - IRawElementProviderFragment.get_BoundingRectangle
---

# IRawElementProviderFragment::get_BoundingRectangle


## -description

Specifies the bounding rectangle of this element.

This property is read-only.

## -parameters

## -remarks

The bounding rectangle is defined by the location of the top left corner on the screen, and the dimensions.

No clipping is required if the element is partly obscured or partly off-screen. The IsOffscreen property should be set to indicate whether the rectangle is actually visible.

Not all points within the bounding rectangle are necessarily clickable.


#### Examples

The following example implementation by a list item provider calculates the bounding rectangle for the item
            based on its height and position within the containing list box.
			


```cpp
HRESULT STDMETHODCALLTYPE ListItemProvider::get_BoundingRectangle(UiaRect * pRetVal)
{
    if (pRetVal == NULL) return E_INVALIDARG;

    UiaRect parentRect;
    HRESULT hr = m_parentProvider->get_BoundingRectangle(&parentRect);
    pRetVal->left = parentRect.left;
    pRetVal->top = parentRect.top + (m_pParentControl->m_itemHeight * m_itemIndex);
    pRetVal->width = parentRect.width;
    pRetVal->height = m_pParentControl->m_itemHeight;
    return S_OK;
}             
```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>