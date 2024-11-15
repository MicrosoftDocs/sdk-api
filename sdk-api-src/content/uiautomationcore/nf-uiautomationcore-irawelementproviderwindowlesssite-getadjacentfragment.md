---
UID: NF:uiautomationcore.IRawElementProviderWindowlessSite.GetAdjacentFragment
title: IRawElementProviderWindowlessSite::GetAdjacentFragment (uiautomationcore.h)
description: Retrieves a fragment pointer for a fragment that is adjacent to the windowless Microsoft ActiveX control owned by this control site.
helpviewer_keywords: ["GetAdjacentFragment","GetAdjacentFragment method [Windows Accessibility]","GetAdjacentFragment method [Windows Accessibility]","IRawElementProviderWindowlessSite interface","IRawElementProviderWindowlessSite interface [Windows Accessibility]","GetAdjacentFragment method","IRawElementProviderWindowlessSite.GetAdjacentFragment","IRawElementProviderWindowlessSite::GetAdjacentFragment","uiautomationcore/IRawElementProviderWindowlessSite::GetAdjacentFragment","winauto.uiauto_IRawElementProviderWindowlessSite_GetAdjacentFragment"]
old-location: winauto\uiauto_IRawElementProviderWindowlessSite_GetAdjacentFragment.htm
tech.root: WinAuto
ms.assetid: 2C43EA00-5C8E-4301-9BFF-9A5D1C585824
ms.date: 12/05/2018
ms.keywords: GetAdjacentFragment, GetAdjacentFragment method [Windows Accessibility], GetAdjacentFragment method [Windows Accessibility],IRawElementProviderWindowlessSite interface, IRawElementProviderWindowlessSite interface [Windows Accessibility],GetAdjacentFragment method, IRawElementProviderWindowlessSite.GetAdjacentFragment, IRawElementProviderWindowlessSite::GetAdjacentFragment, uiautomationcore/IRawElementProviderWindowlessSite::GetAdjacentFragment, winauto.uiauto_IRawElementProviderWindowlessSite_GetAdjacentFragment
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderWindowlessSite::GetAdjacentFragment
 - uiautomationcore/IRawElementProviderWindowlessSite::GetAdjacentFragment
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
 - IRawElementProviderWindowlessSite.GetAdjacentFragment
---

# IRawElementProviderWindowlessSite::GetAdjacentFragment


## -description

Retrieves a fragment pointer for a fragment that is adjacent to the windowless Microsoft ActiveX control  owned by this control site.

## -parameters

### -param direction [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection</a></b>

A value that indicates the adjacent fragment to retrieve (parent, next sibling, previous sibling, and so on).

### -param ppParent [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>**</b>

Receives the adjacent fragment.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.  The return value is E_INVALIDARG if the direction is <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection_FirstChild</a> or <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-navigatedirection">NavigateDirection_LastChild</a>, which are not valid for this method.  If there is no adjacent fragment in the requested direction, the  method returns S_OK and sets <i>ppRetVal</i> to <b>NULL</b>.

## -remarks

To return the parent of the fragment, an object that implements the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> interface must be able to implement the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-navigate">Navigate</a> method.  Implementing <b>Navigate</b> is difficult for a windowless ActiveX control because the control might be unable to determine its location in the accessible tree of the parent object.  The <b>GetAdjacentFragment</b> method enables the windowless ActiveX control to query its site for the adjacent fragment, and then return that fragment to the client that called <b>Navigate</b>.



A provider typically calls this method as part of handling the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-navigate">IRawElementProviderFragment::Navigate</a>  method.


#### Examples

The following C++ code example shows how to implement the <b>GetAdjacentFragment</b> method.


```cpp
IFACEMETHODIMP CProviderWindowlessSite::GetAdjacentFragment(
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
                hr = GetParentProvider(&pSimple);  
                if (SUCCEEDED(hr))  
                {  
                    // Get the parent's IRawElementProviderFragment interface.
                    hr = pSimple->QueryInterface(IID_PPV_ARGS(ppFragment));  
                    pSimple->Release();  
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

```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite">IRawElementProviderWindowlessSite</a>