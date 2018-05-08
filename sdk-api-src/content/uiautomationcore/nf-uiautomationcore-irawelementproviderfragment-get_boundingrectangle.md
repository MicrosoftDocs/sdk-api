---
UID: NF:uiautomationcore.IRawElementProviderFragment.get_BoundingRectangle
title: IRawElementProviderFragment::get_BoundingRectangle
author: windows-driver-content
description: Specifies the bounding rectangle of this element.
old-location: winauto\uiauto_IRawElementProviderFragment_BoundingRectangle.htm
old-project: WinAuto
ms.assetid: 443df4af-06cd-4866-bdeb-b1770ccb9060
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: BoundingRectangle property [Windows Accessibility], BoundingRectangle property [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],BoundingRectangle property, IRawElementProviderFragment.BoundingRectangle, IRawElementProviderFragment.get_BoundingRectangle, IRawElementProviderFragment::BoundingRectangle, IRawElementProviderFragment::get_BoundingRectangle, get_BoundingRectangle, uiauto.uiauto_IRawElementProviderFragment_BoundingRectangle, uiauto_IRawElementProviderFragment_BoundingRectangle, uiautomationcore/IRawElementProviderFragment::BoundingRectangle, uiautomationcore/IRawElementProviderFragment::get_BoundingRectangle, winauto.uiauto_IRawElementProviderFragment_BoundingRectangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	IRawElementProviderFragment.BoundingRectangle
-	IRawElementProviderFragment.get_BoundingRectangle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE ListItemProvider::get_BoundingRectangle(UiaRect * pRetVal)
{
    if (pRetVal == NULL) return E_INVALIDARG;

    UiaRect parentRect;
    HRESULT hr = m_parentProvider-&gt;get_BoundingRectangle(&amp;parentRect);
    pRetVal-&gt;left = parentRect.left;
    pRetVal-&gt;top = parentRect.top + (m_pParentControl-&gt;m_itemHeight * m_itemIndex);
    pRetVal-&gt;width = parentRect.width;
    pRetVal-&gt;height = m_pParentControl-&gt;m_itemHeight;
    return S_OK;
}             </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>
 

 

