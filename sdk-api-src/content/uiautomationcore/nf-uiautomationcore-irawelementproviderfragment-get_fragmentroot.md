---
UID: NF:uiautomationcore.IRawElementProviderFragment.get_FragmentRoot
title: IRawElementProviderFragment::get_FragmentRoot (uiautomationcore.h)
description: Specifies the root node of the fragment.
helpviewer_keywords: ["FragmentRoot property [Windows Accessibility]","FragmentRoot property [Windows Accessibility]","IRawElementProviderFragment interface","IRawElementProviderFragment interface [Windows Accessibility]","FragmentRoot property","IRawElementProviderFragment.FragmentRoot","IRawElementProviderFragment.get_FragmentRoot","IRawElementProviderFragment::FragmentRoot","IRawElementProviderFragment::get_FragmentRoot","get_FragmentRoot","uiauto.uiauto_IRawElementProviderFragment_FragmentRoot","uiauto_IRawElementProviderFragment_FragmentRoot","uiautomationcore/IRawElementProviderFragment::FragmentRoot","uiautomationcore/IRawElementProviderFragment::get_FragmentRoot","winauto.uiauto_IRawElementProviderFragment_FragmentRoot"]
old-location: winauto\uiauto_IRawElementProviderFragment_FragmentRoot.htm
tech.root: WinAuto
ms.assetid: d3fceca3-78b2-4775-ae11-1c9e71dbf772
ms.date: 12/05/2018
ms.keywords: FragmentRoot property [Windows Accessibility], FragmentRoot property [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],FragmentRoot property, IRawElementProviderFragment.FragmentRoot, IRawElementProviderFragment.get_FragmentRoot, IRawElementProviderFragment::FragmentRoot, IRawElementProviderFragment::get_FragmentRoot, get_FragmentRoot, uiauto.uiauto_IRawElementProviderFragment_FragmentRoot, uiauto_IRawElementProviderFragment_FragmentRoot, uiautomationcore/IRawElementProviderFragment::FragmentRoot, uiautomationcore/IRawElementProviderFragment::get_FragmentRoot, winauto.uiauto_IRawElementProviderFragment_FragmentRoot
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
 - IRawElementProviderFragment::get_FragmentRoot
 - uiautomationcore/IRawElementProviderFragment::get_FragmentRoot
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
 - IRawElementProviderFragment.FragmentRoot
 - IRawElementProviderFragment.get_FragmentRoot
---

# IRawElementProviderFragment::get_FragmentRoot


## -description

Specifies the root node of the fragment.

This property is read-only.

## -parameters

## -remarks

A provider for a fragment root should return a pointer to its own implementation of 
			<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>.


#### Examples

The following example implementation for a list item provider returns the provider for the parent list box.
			


```cpp
HRESULT STDMETHODCALLTYPE ListItemProvider::get_FragmentRoot(IRawElementProviderFragmentRoot** pRetVal)
{
    if (pRetVal == NULL) return E_INVALIDARG;
    IRawElementProviderFragmentRoot* pRoot = static_cast<IRawElementProviderFragmentRoot*>(m_parentProvider);
    pRoot->AddRef();
    *pRetVal = pRoot;
    return S_OK;
}            
```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>