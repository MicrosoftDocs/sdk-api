---
UID: NF:iads.IADsPropertyValue.Clear
title: IADsPropertyValue::Clear (iads.h)
description: Clears the current values of the property value object.
helpviewer_keywords: ["Clear","Clear method [ADSI]","Clear method [ADSI]","IADsPropertyValue interface","IADsPropertyValue interface [ADSI]","Clear method","IADsPropertyValue.Clear","IADsPropertyValue::Clear","_ds_iadspropertyvalue_clear","adsi.iadspropertyvalue__clear","adsi.iadspropertyvalue_clear","iads/IADsPropertyValue::Clear"]
old-location: adsi\iadspropertyvalue_clear.htm
tech.root: adsi
ms.assetid: 1662f507-6e1c-4f44-a40d-0eccd8091c51
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [ADSI], Clear method [ADSI],IADsPropertyValue interface, IADsPropertyValue interface [ADSI],Clear method, IADsPropertyValue.Clear, IADsPropertyValue::Clear, _ds_iadspropertyvalue_clear, adsi.iadspropertyvalue__clear, adsi.iadspropertyvalue_clear, iads/IADsPropertyValue::Clear
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
 - IADsPropertyValue::Clear
 - iads/IADsPropertyValue::Clear
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
 - IADsPropertyValue.Clear
---

# IADsPropertyValue::Clear


## -description

The <b>IADsPropertyValue::Clear</b> method clears the current values of the property value object.



## -returns

This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

None


#### Examples

The following code example shows how to use <b>IADsPropertyValue::Clear</b> to clear the value of the "description" property from a property list.


```vb
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Get the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a property entry. If you know the exact type of the property,
' replace ADSTYPE_UNKNOWN with that type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Clear all the values of the property entry.
For Each v In propEntry.Values
    Set propVal = v
    propVal.Clear
Next

propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```


The following code example shows how to use <b>IADsPropertyValue::Clear</b> to clear the value of the "description" property from a property list.


```cpp
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart, lend;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){goto Cleanup;}

 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_UNKNOWN, &var);
if(FAILED(hr)){goto Cleanup;}

pList->Release();
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
if(FAILED(hr)){goto Cleanup;}
VariantClear(&var);
 
// Get the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}
SAFEARRAY *sa = V_ARRAY( &var );
 
// Get the lower and upper bound, iterate, and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    VariantClear(&varItem);
    hr = pVal->Clear();
    if(FAILED(hr)){goto Cleanup;}
}

pList->SetInfo();

Cleanup:
    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pVal)
        pVal->Release();

    if(pObj)
        pObj->Release();

    if(pEnum)
        pEnum->Release();

    if(valStr)
        SysFreeString(valStr);

    VariantClear(&var);
    VariantClear(&varItem);

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a>



<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">IADsPropertyValue Property Methods</a>
