---
UID: NF:uiautomationcore.IRawElementProviderFragment.Navigate
title: IRawElementProviderFragment::Navigate
author: windows-sdk-content
description: Retrieves the Microsoft UI Automation element in a specified direction within the UI Automation tree.
old-location: winauto\uiauto_IRawElementProviderFragment_Navigate.htm
tech.root: WinAuto
ms.assetid: 9e0caf58-a261-4a2b-8e48-368ea3ad8840
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IRawElementProviderFragment interface [Windows Accessibility],Navigate method, IRawElementProviderFragment.Navigate, IRawElementProviderFragment::Navigate, Navigate, Navigate method [Windows Accessibility], Navigate method [Windows Accessibility],IRawElementProviderFragment interface, uiauto.uiauto_IRawElementProviderFragment_Navigate, uiauto_IRawElementProviderFragment_Navigate, uiautomationcore/IRawElementProviderFragment::Navigate, winauto.uiauto_IRawElementProviderFragment_Navigate
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
 - IRawElementProviderFragment.Navigate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderFragment::Navigate


## -description


Retrieves the Microsoft UI Automation element in a specified direction within the UI Automation tree.


## -parameters




### -param arg1

TBD


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>**</b>

Receives a pointer to the provider of the 
				UI Automation element in the specified direction, or <b>NULL</b> if there is no element in that direction.
				This parameter is passed uninitialized.


#### - direction [in]

Type: <b><a href="https://msdn.microsoft.com/33385413-3500-4f80-b53a-fe960d1b53ee">NavigateDirection</a></b>

The direction in which to navigate.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The UI Automation server's implementations of this method define the structure of the UI Automation tree.

Navigation must be supported upward to the parent, downward to the first and last child, and laterally to the next and previous siblings, as applicable.

Each child node has only one parent and must be placed in the chain of siblings reached from the parent by <b>NavigateDirection_FirstChild</b> and <b>NavigateDirection_LastChild</b>.

Relationships among siblings must be identical in both directions: if A is B's previous sibling (<b>NavigateDirection_PreviousSibling</b>), then B is A's next sibling (<b>NavigateDirection_NextSibling</b>). A first child (<b>NavigateDirection_FirstChild</b>) has no previous sibling, and a last child  (<b>NavigateDirection_LastChild</b>) has no next sibling. 

Fragment roots do not enable navigation to a parent or siblings; navigation among fragment roots is handled by the default window providers. Elements in fragments must navigate only to other elements within that fragment.



#### Examples

The following example shows an implementation for a list item provider. The member variables for the parent, 
            previous sibling, and next sibling providers were initialized when the list was created.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*)m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*)m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*)m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag-&gt;AddRef();
    }
    return S_OK;
}              </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>
 

 

