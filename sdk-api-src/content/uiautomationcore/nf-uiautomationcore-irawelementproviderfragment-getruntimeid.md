---
UID: NF:uiautomationcore.IRawElementProviderFragment.GetRuntimeId
title: IRawElementProviderFragment::GetRuntimeId
author: windows-sdk-content
description: Retrieves the runtime identifier of an element.
old-location: winauto\uiauto_IRawElementProviderFragment_GetRuntimeId.htm
tech.root: WinAuto
ms.assetid: e1252353-235e-489e-8eb9-be80d4850ca4
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetRuntimeId, GetRuntimeId method [Windows Accessibility], GetRuntimeId method [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],GetRuntimeId method, IRawElementProviderFragment.GetRuntimeId, IRawElementProviderFragment::GetRuntimeId, uiauto.uiauto_IRawElementProviderFragment_GetRuntimeId, uiauto_IRawElementProviderFragment_GetRuntimeId, uiautomationcore/IRawElementProviderFragment::GetRuntimeId, winauto.uiauto_IRawElementProviderFragment_GetRuntimeId
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
 - IRawElementProviderFragment.GetRuntimeId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderFragment::GetRuntimeId


## -description


Retrieves the runtime identifier of an element.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives a pointer to the runtime identifier. This parameter is passed uninitialized.
				


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implementations should return <b>NULL</b> for a top-level element that is hosted in a window. 
			Other elements should return an array that contains <b>UiaAppendRuntimeId</b> 
            (defined in Uiautomationcoreapi.h), 
			followed by a value that is unique within an instance of the fragment.



#### Examples

The following implementation for a list item returns a runtime identifier made up of the 
            <b>UiaAppendRuntimeId</b>constant and the index of the item within the list.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE ListItemProvider::GetRuntimeId(SAFEARRAY ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }
    
    int rId[] = { UiaAppendRuntimeId, m_itemIndex };
    SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);
    if (psa == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    for (LONG i = 0; i &lt; 2; i++)
    {
        SafeArrayPutElement(psa, &amp;i, (void*)&amp;(rId[i]));
    }
    
    *pRetVal = psa;
    return S_OK;
}   </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>



<b>Reference</b>
 

 

