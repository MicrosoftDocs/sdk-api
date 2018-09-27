---
UID: NF:iads.IADsPropertyList.Item
title: IADsPropertyList::Item
author: windows-sdk-content
description: The IADsPropertyList::Item method retrieves the specified property item from the list.
old-location: adsi\iadspropertylist_item.htm
tech.root: ADSI
ms.assetid: 6e103872-ea2e-4178-9c8a-b958ae3bcf85
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IADsPropertyList interface [ADSI],Item method, IADsPropertyList.Item, IADsPropertyList::Item, Item, Item method [ADSI], Item method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_item, adsi.iadspropertylist__item, adsi.iadspropertylist_item, iads/IADsPropertyList::Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPropertyList.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsPropertyList::Item


## -description


The <b>IADsPropertyList::Item</b> method retrieves the specified property item from the list.


## -parameters




### -param varIndex [in]

The <b>VARIANT</b> that contains the index or name of the property to be retrieved.


### -param pVariant [in, out]

Address of a caller-allocated <b>VARIANT</b> variable. On return, the <b>VARIANT</b> contains the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> pointer to the object which implements the  <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> interface for the attribute retrieved.


## -returns



This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



You must clear <i>pVariant</i> using <b>VariantClear</b> when the value returned by the <b>Item</b> method is no longer required.


#### Examples

The following code example shows how to enumerate all the entries with the <b>Item</b> method.


```vb
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc02/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "No of Property Found: " & count
 
'==== Getting the property list item with Name ==================
Set propEntry = propList.Item("uSNCreated")
Debug.Print propEntry.Name
Debug.Print propEntry.ADsType
 
' to examine property entries by name and type 
For i = 0 To count - 1
    '==== Getting the property list item with Number =============
    Set propEntry = propList.Item(i)
    Debug.Print propEntry.Name
    Debug.Print propEntry.ADsType
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
    Set propEntry = Nothing

```


The following code example shows how to retrieve the <b>Owner</b> property of a computer using the <b>IADsPropertyList::Item</b> method. For more information about the <b>GetPropertyCache</b>  function and a code example, see <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>.


```cpp
////////////////////////////////////////
// function:    PropertyItem
//    input:    PropertyList, 
//              name of the item
//   output:    Property entry
//     uses:    IADsPropertyList::Item
////////////////////////////////////////
IADsPropertyEntry *PropertyItem(
         IADsPropertyList *pList,
         LPWSTR item)
{
    IADsPropertyEntry *pEntry;
    VARIANT varEntry, varItem;

    if(!pList || !item)
    {
        _tprintf(TEXT("Invalid parameter..."));
        return NULL;
    }

    VariantInit(&varItem);
    VariantInit(&varEntry);
 
    // get a property entry
    V_BSTR(&varItem)= SysAllocString(item);
    V_VT(&varItem)=VT_BSTR;
    HRESULT hr = pList->Item(varItem ,&varEntry);
    hr = V_DISPATCH(&var)->QueryInterface(
                        IID_IADsPropertyEntry,
                        (void**)&pEntry);
    VariantClear(&varItem);
    VariantClear(&varEntry);
    return pEntry;
}
 
///////////////////////////////////////
// examine a property entry
///////////////////////////////////////
IADsPropertyList *pList; pList=GetPropertyCache(L"WinNT://myComputer,computer");
 
IADsPropertyEntry *pEntry;
pEntry = PropertyItem(pList, L"Owner");

if(pEntry)
{
    HRESULT hr;
    BSTR bstr;
    long ln;

    hr = pEntry->get_Name(&bstr);
    if(SUCCEEDED(hr))
    {
        SysFreeString(bstr);
    }
    printf(" Name : %S\n", bstr);
 
    pEntry->get_ADsType(&ln);
    if(SUCCEEDED(hr))
    {
        printf(" Type : %d\n", ln);
    }
 
    pEntry->get_ControlCode(&ln); 
    if(SUCCEEDED(hr))
    {
        printf(" Code %d\n",ln);
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

