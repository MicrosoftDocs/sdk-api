---
UID: NF:uiautomationcore.IRawElementProviderWindowlessSite.GetRuntimeIdPrefix
title: IRawElementProviderWindowlessSite::GetRuntimeIdPrefix (uiautomationcore.h)
description: Retrieves a Microsoft UI Automation runtime ID that is unique to the windowless Microsoft ActiveX control site.
helpviewer_keywords: ["GetRuntimeIdPrefix","GetRuntimeIdPrefix method [Windows Accessibility]","GetRuntimeIdPrefix method [Windows Accessibility]","IRawElementProviderWindowlessSite interface","IRawElementProviderWindowlessSite interface [Windows Accessibility]","GetRuntimeIdPrefix method","IRawElementProviderWindowlessSite.GetRuntimeIdPrefix","IRawElementProviderWindowlessSite::GetRuntimeIdPrefix","uiautomationcore/IRawElementProviderWindowlessSite::GetRuntimeIdPrefix","winauto.uiauto_IRawElementProviderWindowlessSite_getRuntimeIdPrefix"]
old-location: winauto\uiauto_IRawElementProviderWindowlessSite_getRuntimeIdPrefix.htm
tech.root: WinAuto
ms.assetid: E10BBE53-5AAB-4BAB-AFC8-866224011E43
ms.date: 12/05/2018
ms.keywords: GetRuntimeIdPrefix, GetRuntimeIdPrefix method [Windows Accessibility], GetRuntimeIdPrefix method [Windows Accessibility],IRawElementProviderWindowlessSite interface, IRawElementProviderWindowlessSite interface [Windows Accessibility],GetRuntimeIdPrefix method, IRawElementProviderWindowlessSite.GetRuntimeIdPrefix, IRawElementProviderWindowlessSite::GetRuntimeIdPrefix, uiautomationcore/IRawElementProviderWindowlessSite::GetRuntimeIdPrefix, winauto.uiauto_IRawElementProviderWindowlessSite_getRuntimeIdPrefix
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
 - IRawElementProviderWindowlessSite::GetRuntimeIdPrefix
 - uiautomationcore/IRawElementProviderWindowlessSite::GetRuntimeIdPrefix
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
 - IRawElementProviderWindowlessSite.GetRuntimeIdPrefix
---

# IRawElementProviderWindowlessSite::GetRuntimeIdPrefix


## -description

Retrieves a Microsoft UI Automation runtime ID that is unique to the windowless Microsoft ActiveX control site.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives the runtime ID.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A UI Automation fragment must implement the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid">IRawElementProviderFragment::GetRuntimeId</a> method to return a unique ID for the fragment.  This is difficult for a windowless ActiveX control, which must be able to identify itself as unique among other windowless controls in the ActiveX control container.  To resolve this issue, the windowless site should implement the <b>GetRuntimeIdPrefix</b>  method by forming a <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains the constant <b>UiaAppendRuntimeId</b>, followed by an integer value that is unique to this windowless site.  

The fragment can then append an integer value that is unique relative to all other fragments in the windowless ActiveX control, and return it to the client.  



For example, the site might return a SAFEARRAY with the following contents: <code>{ UiaAppendRuntimeId, 3 }</code>.  This might represent the third ActiveX control in the container.  The fragment provider's <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid">GetRuntimeId</a> method could then form a SAFEARRAY with the following contents: <code>{ UiaAppendRuntimeId, 3, 5 }</code>.  This might represent the fifth fragment within the ActiveX container.  The whole SAFEARRAY would be a unique ID relative to the whole ActiveX control container.



A provider typically calls this method as part of handling the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid">GetRuntimeId</a> method.


#### Examples

The following C++ code example shows how to implement the <b>GetRuntimeIdPrefix</b> method.


```cpp
IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
     SAFEARRAY **ppsaPrefix)   
{   
    if (ppsaPrefix == NULL) 
    {
        return E_INVALIDARG;
    }

    // m_siteIndex is the index of the windowless control's
    // site. It is defined by the control container.
    int rId[] = { UiaAppendRuntimeId, m_siteIndex };
    SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
    if (psa == NULL)
    {
        return E_OUTOFMEMORY;
    }

    for (LONG i = 0; i < 2; i++)
    {
        SafeArrayPutElement(psa, &i, (void*)&(rId[i]));
    }

    *ppsaPrefix = psa;  
    return S_OK;  
}  

```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite">IRawElementProviderWindowlessSite</a>