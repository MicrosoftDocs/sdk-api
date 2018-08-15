---
UID: NF:uiautomationcore.IRawElementProviderFragment.get_FragmentRoot
title: IRawElementProviderFragment::get_FragmentRoot
author: windows-sdk-content
description: Specifies the root node of the fragment.
old-location: winauto\uiauto_IRawElementProviderFragment_FragmentRoot.htm
old-project: WinAuto
ms.assetid: d3fceca3-78b2-4775-ae11-1c9e71dbf772
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FragmentRoot property [Windows Accessibility], FragmentRoot property [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],FragmentRoot property, IRawElementProviderFragment.FragmentRoot, IRawElementProviderFragment.get_FragmentRoot, IRawElementProviderFragment::FragmentRoot, IRawElementProviderFragment::get_FragmentRoot, get_FragmentRoot, uiauto.uiauto_IRawElementProviderFragment_FragmentRoot, uiauto_IRawElementProviderFragment_FragmentRoot, uiautomationcore/IRawElementProviderFragment::FragmentRoot, uiautomationcore/IRawElementProviderFragment::get_FragmentRoot, winauto.uiauto_IRawElementProviderFragment_FragmentRoot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
 - IRawElementProviderFragment.FragmentRoot
 - IRawElementProviderFragment.get_FragmentRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderFragment::get_FragmentRoot


## -description


Specifies the root node of the fragment.

This property is read-only.


## -parameters


## -remarks



A provider for a fragment root should return a pointer to its own implementation of 
			<a href="https://msdn.microsoft.com/16e51962-915e-40ea-a7a1-6f5a5809ba05">IRawElementProviderFragmentRoot</a>.


#### Examples

The following example implementation for a list item provider returns the provider for the parent list box.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE ListItemProvider::get_FragmentRoot(IRawElementProviderFragmentRoot** pRetVal)
{
    if (pRetVal == NULL) return E_INVALIDARG;
    IRawElementProviderFragmentRoot* pRoot = static_cast&lt;IRawElementProviderFragmentRoot*&gt;(m_parentProvider);
    pRoot-&gt;AddRef();
    *pRetVal = pRoot;
    return S_OK;
}            </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>
 

 

