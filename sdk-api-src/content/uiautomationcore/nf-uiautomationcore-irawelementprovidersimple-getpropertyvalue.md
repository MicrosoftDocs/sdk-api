---
UID: NF:uiautomationcore.IRawElementProviderSimple.GetPropertyValue
title: IRawElementProviderSimple::GetPropertyValue (uiautomationcore.h)
description: Retrieves the value of a property supported by the Microsoft UI Automation provider.
helpviewer_keywords: ["GetPropertyValue","GetPropertyValue method [Windows Accessibility]","GetPropertyValue method [Windows Accessibility]","IRawElementProviderSimple interface","IRawElementProviderSimple interface [Windows Accessibility]","GetPropertyValue method","IRawElementProviderSimple.GetPropertyValue","IRawElementProviderSimple::GetPropertyValue","uiauto.uiauto_IRawElementProviderSimple_GetPropertyValue","uiauto_IRawElementProviderSimple_GetPropertyValue","uiautomationcore/IRawElementProviderSimple::GetPropertyValue","winauto.uiauto_IRawElementProviderSimple_GetPropertyValue"]
old-location: winauto\uiauto_IRawElementProviderSimple_GetPropertyValue.htm
tech.root: WinAuto
ms.assetid: 029ea063-009d-4b54-978a-4183454b2d66
ms.date: 12/05/2018
ms.keywords: GetPropertyValue, GetPropertyValue method [Windows Accessibility], GetPropertyValue method [Windows Accessibility],IRawElementProviderSimple interface, IRawElementProviderSimple interface [Windows Accessibility],GetPropertyValue method, IRawElementProviderSimple.GetPropertyValue, IRawElementProviderSimple::GetPropertyValue, uiauto.uiauto_IRawElementProviderSimple_GetPropertyValue, uiauto_IRawElementProviderSimple_GetPropertyValue, uiautomationcore/IRawElementProviderSimple::GetPropertyValue, winauto.uiauto_IRawElementProviderSimple_GetPropertyValue
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
 - IRawElementProviderSimple::GetPropertyValue
 - uiautomationcore/IRawElementProviderSimple::GetPropertyValue
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
 - IRawElementProviderSimple.GetPropertyValue
---

# IRawElementProviderSimple::GetPropertyValue


## -description

Retrieves the value of a property supported by the Microsoft UI Automation provider.

## -parameters

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

Receives the property value, or <b>VT_EMPTY</b> if the property is not supported by this
				provider. This parameter is passed uninitialized. See Remarks.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an  <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code.

If the provider does not support the <i>propertyId</i> property, the provider should set <i>pRetVal-&gt;vt</i> to <b>VT_EMPTY</b> and return <b>S_OK</b>.

## -remarks

If a provider is explicitly hiding the property value (that is, the provider does not supply the property, and the request is not to be passed through to other providers), it should return a pointer obtained by using the             <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue">UiaGetReservedNotSupportedValue</a> function. For example: 
            


```
pRetVal->vt = VT_UNKNOWN;
UiaGetReservedNotSupportedValue(&pRetVal->punkVal);
```


UI Automation properties of the <b>double</b> type support Not a Number (NaN) values. When returning a NaN value, the provider should return a quiet (non-signaling) NaN to avoid raising an exception if floating-point exceptions are turned on. The following example shows how to create a quiet NaN:

            


```
ULONGLONG ulNaN = 0xFFFFFFFFFFFFFFFF;
    *pRetVal = *reinterpret_cast<double*>(&ulNaN);
```


Alternatively, you can use the following function from the standard C++ libraries:


```
numeric_limits<double>::quiet_NaN( )
```



#### Examples

The following example returns various property values. The <b>UiaIds</b> structure contains
            property identifiers; to see how it is initialized, see <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uialookupid">UiaLookupId</a>.
			


```cpp

HRESULT STDMETHODCALLTYPE Provider::GetPropertyValue(PROPERTYID propertyId, 
        VARIANT* pRetVal)
{
    if (propertyId == UiaIds.ControlTypeProperty)
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UiaIds.ButtonControlType;
    }

    // The Name property normally comes from the Caption property of the 
    // control window, if it has one. The Name is overridden here for the 
    // sake of illustration. 
    else if (propertyId == UiaIds.NameProperty)
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"ColorButton");
    }
    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the host 
        //window provider.
    }
    return S_OK;
}
            
```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>