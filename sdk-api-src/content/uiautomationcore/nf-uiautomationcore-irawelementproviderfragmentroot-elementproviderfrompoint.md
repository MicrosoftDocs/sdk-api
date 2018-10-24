---
UID: NF:uiautomationcore.IRawElementProviderFragmentRoot.ElementProviderFromPoint
title: IRawElementProviderFragmentRoot::ElementProviderFromPoint
author: windows-sdk-content
description: Retrieves the provider of the element that is at the specified point in this fragment.
old-location: winauto\uiauto_IRawElementProviderFragmentRoot_ElementProviderFromPoint.htm
tech.root: WinAuto
ms.assetid: 469149c7-8c2c-468c-b7cc-6d849de427f1
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: ElementProviderFromPoint, ElementProviderFromPoint method [Windows Accessibility], ElementProviderFromPoint method [Windows Accessibility],IRawElementProviderFragmentRoot interface, IRawElementProviderFragmentRoot interface [Windows Accessibility],ElementProviderFromPoint method, IRawElementProviderFragmentRoot.ElementProviderFromPoint, IRawElementProviderFragmentRoot::ElementProviderFromPoint, uiauto.uiauto_IRawElementProviderFragmentRoot_ElementProviderFromPoint, uiauto_IRawElementProviderFragmentRoot_ElementProviderFromPoint, uiautomationcore/IRawElementProviderFragmentRoot::ElementProviderFromPoint, winauto.uiauto_IRawElementProviderFragmentRoot_ElementProviderFromPoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderFragmentRoot.ElementProviderFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderFragmentRoot::ElementProviderFromPoint


## -description


Retrieves the provider of the element that is at the specified point in this fragment.


## -parameters




### -param x [in]

Type: <b>double</b>

The horizontal screen coordinate.


### -param y [in]

Type: <b>double</b>

The vertical screen coordinate.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>**</b>

Receives a pointer to the provider of the element at (x, y),	or <b>NULL</b> if none exists. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned provider should correspond to the element that would receive mouse input at the specified point.

If the point is on this element but not on any child element, either <b>NULL</b> or the provider of the fragment root is returned. If the point is on an element in another framework that is hosted by this fragment, the method returns the element that hosts that fragment (as indicated by <a href="https://msdn.microsoft.com/3e64956d-5ab3-46b6-87db-4b0770c8f89a">IRawElementProviderFragment::GetEmbeddedFragmentRoots</a>).


#### Examples

The following example shows an implementation for a list box hosted in an <b>HWND</b> 
            whose handle is <i>m_controlHwnd</i>. 
            IndexFromY retrieves the index of the list item at the cursor position, 
            and GetItemByIndex retrieves
            the UI Automation provider for that item. 
			


```cpp
HRESULT STDMETHODCALLTYPE ListProvider::ElementProviderFromPoint(double x, double y, IRawElementProviderFragment** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }
    POINT pt;
    pt.x = (LONG)x;
    pt.y = (LONG)y;
    ScreenToClient(m_controlHwnd, &pt);
    int itemIndex = this->m_pControl->IndexFromY(m_controlHwnd, pt.y);
    ListItemProvider* pItem = GetItemByIndex(itemIndex);  
    if (pItem != NULL)
    {
        *pRetVal = (IRawElementProviderFragment*)pItem;
        pItem->AddRef();
    }
    else 
    {
        pRetVal = (IRawElementProviderFragment*)this;
        pItem->AddRef();
    }

    return S_OK;
}            
```





## -see-also




<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>
 

 

