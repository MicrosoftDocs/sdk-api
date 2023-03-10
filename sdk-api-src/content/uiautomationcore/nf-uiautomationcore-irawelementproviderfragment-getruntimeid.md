---
UID: NF:uiautomationcore.IRawElementProviderFragment.GetRuntimeId
title: IRawElementProviderFragment::GetRuntimeId (uiautomationcore.h)
description: Retrieves the runtime identifier of an element.
helpviewer_keywords: ["GetRuntimeId","GetRuntimeId method [Windows Accessibility]","GetRuntimeId method [Windows Accessibility]","IRawElementProviderFragment interface","IRawElementProviderFragment interface [Windows Accessibility]","GetRuntimeId method","IRawElementProviderFragment.GetRuntimeId","IRawElementProviderFragment::GetRuntimeId","uiauto.uiauto_IRawElementProviderFragment_GetRuntimeId","uiauto_IRawElementProviderFragment_GetRuntimeId","uiautomationcore/IRawElementProviderFragment::GetRuntimeId","winauto.uiauto_IRawElementProviderFragment_GetRuntimeId"]
old-location: winauto\uiauto_IRawElementProviderFragment_GetRuntimeId.htm
tech.root: WinAuto
ms.assetid: e1252353-235e-489e-8eb9-be80d4850ca4
ms.date: 12/05/2018
ms.keywords: GetRuntimeId, GetRuntimeId method [Windows Accessibility], GetRuntimeId method [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],GetRuntimeId method, IRawElementProviderFragment.GetRuntimeId, IRawElementProviderFragment::GetRuntimeId, uiauto.uiauto_IRawElementProviderFragment_GetRuntimeId, uiauto_IRawElementProviderFragment_GetRuntimeId, uiautomationcore/IRawElementProviderFragment::GetRuntimeId, winauto.uiauto_IRawElementProviderFragment_GetRuntimeId
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
 - IRawElementProviderFragment::GetRuntimeId
 - uiautomationcore/IRawElementProviderFragment::GetRuntimeId
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
 - IRawElementProviderFragment.GetRuntimeId
---

# IRawElementProviderFragment::GetRuntimeId


## -description

Retrieves the runtime identifier of an element.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to the runtime identifier. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implementations should return <b>NULL</b> for a top-level element that is hosted in a window. 
			Other elements should return an array that contains <b>UiaAppendRuntimeId</b> 
            (defined in Uiautomationcoreapi.h), 
			followed by a value that is unique within an instance of the fragment.



#### Examples

The following implementation for a list item returns a runtime identifier made up of the 
           <b>UiaAppendRuntimeId</b> constant and the index of the item within the list.
			


```cpp
HRESULT STDMETHODCALLTYPE ListItemProvider::GetRuntimeId(SAFEARRAY ** pRetVal)
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
    
    for (LONG i = 0; i < 2; i++)
    {
        SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
    }
    
    *pRetVal = psa;
    return S_OK;
}   
```

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<b>Reference</b>