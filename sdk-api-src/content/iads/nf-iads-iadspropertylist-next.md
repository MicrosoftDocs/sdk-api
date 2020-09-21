---
UID: NF:iads.IADsPropertyList.Next
title: IADsPropertyList::Next (iads.h)
description: The IADsPropertyList::Next method gets the next item in the property list. The returned item is a Property Entry object.
helpviewer_keywords: ["IADsPropertyList interface [ADSI]","Next method","IADsPropertyList.Next","IADsPropertyList::Next","Next","Next method [ADSI]","Next method [ADSI]","IADsPropertyList interface","_ds_iadspropertylist_next","adsi.iadspropertylist__next","adsi.iadspropertylist_next","iads/IADsPropertyList::Next"]
old-location: adsi\iadspropertylist_next.htm
tech.root: adsi
ms.assetid: 2a12ba88-363b-41e3-bd05-8a71f5317097
ms.date: 12/05/2018
ms.keywords: IADsPropertyList interface [ADSI],Next method, IADsPropertyList.Next, IADsPropertyList::Next, Next, Next method [ADSI], Next method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_next, adsi.iadspropertylist__next, adsi.iadspropertylist_next, iads/IADsPropertyList::Next
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
 - IADsPropertyList::Next
 - iads/IADsPropertyList::Next
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
 - IADsPropertyList.Next
---

# IADsPropertyList::Next


## -description

The <b>IADsPropertyList::Next</b> method gets the next item in the property list. The returned item is a Property Entry object.

## -parameters

### -param pVariant [out]

Address of a caller-allocated variable that contains the value of the next item in the property list. The return value of <b>VT_DISPATCH</b> refers to an  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to an object implementing the  <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> interface.

## -returns

This method supports the standard <b>HRESULT</b> values, including <b>S_OK</b> if the item is obtained. When the last item in the list is returned, the return value that is returned will differ depending on which provider is used. The following codes are used to indicate that the last item in the list was obtained:

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

You must clear <i>pVariant</i> using <b>VariantClear</b> when the value returned by the <b>Next</b> method is no longer required.


#### Examples

The following code example shows how to walk through a property list using the <b>Next</b> method.


```vb
Dim propList As IADsPropertyList
Dim v as Variant
Dim propVal As IADsPropertyValue
 
On Error Resume Next
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
Set v = propList.Next()
While (Not (IsNull(v)) And Err.Number = 0)
    Set propEnty = v
    Debug.Print v.Name
    Debug.Print v.AdsType
    
    Set v = propList.Next    
Wend
```


The following C++ code example shows how to work the <b>IADsPropertyList::Next</b> method.


```cpp
////////////////////////////////////
// Function used to retrieve an entry using the 
// IADsPropertyList::Next method.
 
//     name: GetNextEntry
//    input: IADsPropertyList*
//   return: IADsPropertyEntry
//     uses: IADsPropertyList::Next
/////////////////////////////////////////////////////////
IADsPropertyEntry* GetNextEntry(IADsPropertyList* pList)
{
    VARIANT var;
    VariantInit(&var);
    IADsPropertyEntry *pEntry;

    if(!pList)
    {
        _tprintf("An error has occurred.");
        return NULL;
    }
 
    HRESULT hr = pList->Next(&var);
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                         (void**)&pEntry);
    VariantClear(&var);
    return pEntry;
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>