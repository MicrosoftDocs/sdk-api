---
UID: NN:iads.IADsClass
title: IADsClass (iads.h)
description: The IADsClass interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include IADsProperty for attribute definitions and IADsSyntax for attribute syntax.
helpviewer_keywords: ["IADsClass","IADsClass interface [ADSI]","IADsClass interface [ADSI]","described","_ds_iadsclass","adsi.iadsclass","iads/IADsClass"]
old-location: adsi\iadsclass.htm
tech.root: adsi
ms.assetid: 690b0c96-6319-42d8-8b0e-c43f46f91031
ms.date: 12/05/2018
ms.keywords: IADsClass, IADsClass interface [ADSI], IADsClass interface [ADSI],described, _ds_iadsclass, adsi.iadsclass, iads/IADsClass
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsClass
 - iads/IADsClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsClass
---

# IADsClass interface


## -description

The <b>IADsClass</b> interface is designed for managing schema class objects that provide class definitions for any ADSI object. Other schema management interfaces include  <a href="/windows/desktop/api/iads/nn-iads-iadsproperty">IADsProperty</a> for attribute definitions and  <a href="/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a> for attribute syntax.

## -inheritance

The <b>IADsClass</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsClass</b> also has these types of members:

## -remarks

Schema objects are organized in the schema container of a given directory. To access an object's schema class, use the object's <b>Schema</b> property (namely, call the <a href="/windows/desktop/ADSI/iads-property-methods">IADs::get_Schema</a> property method) to obtain the ADsPath string and use that string to bind to its schema class object.


#### Examples

The following code example shows how to implement the <b>IADsClass</b> interface.


```vb
Dim obj As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cls = GetObject(obj.Schema)
 
' Inspecting mandatory and optional properties.
For Each p In cls.MandatoryProperties
    MsgBox "Must-have: " & p
Next
For Each p In cls.OptionalProperties
    MsgBox "May-have: " & p
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cls = Nothing
```


The following code example shows how to implement the <b>IADsClass</b> interface.


```cpp
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) { goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) { goto Cleanup; }
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) { goto Cleanup; }
 
VariantInit(&var);
pCls->get_MandatoryProperties(&var);
hr = printVarArray(var);
 
VariantClear(&var);
pCls->get_OptionalProperties(&var);
hr = printVarArray(var);

Cleanup:
    if(pCls)
        pCls->Release();

    if(pADs)
        pADs->Release();

    SysFreeString(bstrSchema);
    VariantClear(&var);
    CoUninitialize();
    return hr;
```


The following code example shows how to implement the <b>printVarArray</b> function.


```cpp
HRESULT printVarArray(VARIANT var)
{
    LONG lstart, lend;
    VARIANT varItem;
    HRESULT hr;
    SAFEARRAY *sa = V_ARRAY( &var );
    hr = SafeArrayGetLBound( sa, 1, &lstart );
    hr = SafeArrayGetUBound( sa, 1, &lend );
    VariantInit(&varItem);
    for ( long idx=lstart; idx <= lend; idx++ ) {
        hr = SafeArrayGetElement( sa, &idx, &varItem );
        printf("   %S \n", V_BSTR(&varItem));
        VariantClear(&varItem);
    }
    printf("\n");
    return S_OK;
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsproperty">IADsProperty</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssyntax">IADsSyntax</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
