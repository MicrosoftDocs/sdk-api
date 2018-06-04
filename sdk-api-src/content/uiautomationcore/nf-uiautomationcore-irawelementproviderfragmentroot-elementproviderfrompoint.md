---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE ListProvider::ElementProviderFromPoint(double x, double y, IRawElementProviderFragment** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }
    POINT pt;
    pt.x = (LONG)x;
    pt.y = (LONG)y;
    ScreenToClient(m_controlHwnd, &amp;pt);
    int itemIndex = this-&gt;m_pControl-&gt;IndexFromY(m_controlHwnd, pt.y);
    ListItemProvider* pItem = GetItemByIndex(itemIndex);  
    if (pItem != NULL)
    {
        *pRetVal = (IRawElementProviderFragment*)pItem;
        pItem-&gt;AddRef();
    }
    else 
    {
        pRetVal = (IRawElementProviderFragment*)this;
        pItem-&gt;AddRef();
    }

    return S_OK;
}            </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>
 

 

