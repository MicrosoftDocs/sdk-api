---
UID: NF:uiautomationcore.IRawElementProviderWindowlessSite.GetAdjacentFragment
title: IRawElementProviderWindowlessSite::GetAdjacentFragment
author: windows-sdk-content
description: Retrieves a fragment pointer for a fragment that is adjacent to the windowless Microsoft ActiveX control owned by this control site.
old-location: winauto\uiauto_IRawElementProviderWindowlessSite_GetAdjacentFragment.htm
old-project: WinAuto
ms.assetid: 2C43EA00-5C8E-4301-9BFF-9A5D1C585824
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetAdjacentFragment, GetAdjacentFragment method [Windows Accessibility], GetAdjacentFragment method [Windows Accessibility],IRawElementProviderWindowlessSite interface, IRawElementProviderWindowlessSite interface [Windows Accessibility],GetAdjacentFragment method, IRawElementProviderWindowlessSite.GetAdjacentFragment, IRawElementProviderWindowlessSite::GetAdjacentFragment, uiautomationcore/IRawElementProviderWindowlessSite::GetAdjacentFragment, winauto.uiauto_IRawElementProviderWindowlessSite_GetAdjacentFragment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderWindowlessSite.GetAdjacentFragment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderWindowlessSite::GetAdjacentFragment


## -description


Retrieves a fragment pointer for a fragment that is adjacent to the windowless Microsoft ActiveX control  owned by this control site.


## -parameters




### -param direction [in]

Type: <b><a href="https://msdn.microsoft.com/33385413-3500-4f80-b53a-fe960d1b53ee">NavigateDirection</a></b>

A value that indicates the adjacent fragment to retrieve (parent, next sibling, previous sibling, and so on).  


### -param ppParent






#### - ppRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>**</b>

Receives the adjacent fragment.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.  The return value is E_INVALIDARG if the direction is <a href="uiauto_NavDirEnum.htm">NavigateDirection_FirstChild</a> or <a href="uiauto_NavDirEnum.htm">NavigateDirection_LastChild</a>, which are not valid for this method.  If there is no adjacent fragment in the requested direction, the  method returns S_OK and sets <i>ppRetVal</i> to <b>NULL</b>.






## -remarks



To return the parent of the fragment, an object that implements the <a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a> interface must be able to implement the <a href="https://msdn.microsoft.com/9e0caf58-a261-4a2b-8e48-368ea3ad8840">Navigate</a> method.  Implementing <b>Navigate</b> is difficult for a windowless ActiveX control because the control might be unable to determine its location in the accessible tree of the parent object.  The <b>GetAdjacentFragment</b> method enables the windowless ActiveX control to query its site for the adjacent fragment, and then return that fragment to the client that called <b>Navigate</b>.



A provider typically calls this method as part of handling the <a href="https://msdn.microsoft.com/9e0caf58-a261-4a2b-8e48-368ea3ad8840">IRawElementProviderFragment::Navigate</a>  method.


#### Examples

The following C++ code example shows how to implement the <b>GetAdjacentFragment</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
        enum NavigateDirection direction, IRawElementProviderFragment **ppFragment)   
{
    if (ppFragment == NULL)
    {
        return E_INVALIDARG;
    }
    
    *ppFragment = NULL;
    HRESULT hr = S_OK;

    switch (direction)
    {
        case NavigateDirection_Parent:
            {  
                IRawElementProviderSimple *pSimple = NULL;

                // Call an application-defined function to retrieve the
                // parent provider interface.
                hr = GetParentProvider(&amp;pSimple);  
                if (SUCCEEDED(hr))  
                {  
                    // Get the parent's IRawElementProviderFragment interface.
                    hr = pSimple-&gt;QueryInterface(IID_PPV_ARGS(ppFragment));  
                    pSimple-&gt;Release();  
                } 
            }  
            break;  
  
        case NavigateDirection_FirstChild:
        case NavigateDirection_LastChild:
            hr = E_INVALIDARG;
            break;

        // Ignore NavigateDirection_NextSibling and NavigateDirection_PreviousSibling
        // because there are no adjacent fragments.
        default:  
            break;  
    }  
  
    return hr;  
}   
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/E6BE069B-C639-4578-9E5F-8CFE1267A847">IRawElementProviderWindowlessSite</a>
 

 

