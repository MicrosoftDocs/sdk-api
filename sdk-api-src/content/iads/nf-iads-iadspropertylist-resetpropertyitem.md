---
UID: NF:iads.IADsPropertyList.ResetPropertyItem
title: IADsPropertyList::ResetPropertyItem (iads.h)
description: Removes the specified item from the list; that is, from the cache.
helpviewer_keywords: ["IADsPropertyList interface [ADSI]","ResetPropertyItem method","IADsPropertyList.ResetPropertyItem","IADsPropertyList::ResetPropertyItem","ResetPropertyItem","ResetPropertyItem method [ADSI]","ResetPropertyItem method [ADSI]","IADsPropertyList interface","_ds_iadspropertylist_resetpropertyitem","adsi.iadspropertylist__resetpropertyitem","adsi.iadspropertylist_resetpropertyitem","iads/IADsPropertyList::ResetPropertyItem"]
old-location: adsi\iadspropertylist_resetpropertyitem.htm
tech.root: adsi
ms.assetid: 25ee4444-476d-4146-ac22-3b0cfed3f2c0
ms.date: 12/05/2018
ms.keywords: IADsPropertyList interface [ADSI],ResetPropertyItem method, IADsPropertyList.ResetPropertyItem, IADsPropertyList::ResetPropertyItem, ResetPropertyItem, ResetPropertyItem method [ADSI], ResetPropertyItem method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_resetpropertyitem, adsi.iadspropertylist__resetpropertyitem, adsi.iadspropertylist_resetpropertyitem, iads/IADsPropertyList::ResetPropertyItem
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
 - IADsPropertyList::ResetPropertyItem
 - iads/IADsPropertyList::ResetPropertyItem
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
 - IADsPropertyList.ResetPropertyItem
---

# IADsPropertyList::ResetPropertyItem


## -description

The <b>IADsPropertyList::ResetPropertyItem</b> method removes the specified item from the list; that is, from the cache. You can specify the item to be removed by name (as a string) or by index (as an integer).

## -parameters

### -param varEntry [in]

Entry to be reset.

## -returns

This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b>. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

<b>ResetPropertyItem</b> only affects the contents of the cache and does not affect the properties on the actual object in the directory; that is calling  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a> after calling <b>ResetPropertyItem</b> does not delete the properties on the directory object.


#### Examples

The following code example shows how to implement <b>ResetPropertyItem</b>.


```vb
Dim propList As IADsPropertyList

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
 
'--- Now modify the cache using PutPropertyItem
Set propVal = New PropertyValue
'--- Property Value-----
propVal.CaseIgnoreString = "Fabrikam"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'--- Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' --- Property List----
propList.PutPropertyItem (propEntry)
 
' Commit to the directory. Without this, the changes take place only in the cache.
propList.SetInfo 
 
propList.GetInfo
Debug.Print " Number of Properties = " & propList.PropertyCount
propList.ResetPropertyItem "adminDescription"
 
' the property count should have been reduced by one.
Debug.Print "Number of properties = " & propList.PropertyCount

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propVal = Nothing
    Set propEntry = Nothing

```


The following code example shows the effect produced by a call to <b>IADsPropertyList::ResetPropertyItem</b>. For more information and the listing of the <b>GetPropertyCache</b> function, see  <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>. For more information and the listing of the <b>GetNextEntry</b> and <b>PropertyItem</b> functions, see  <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-next">IADsPropertyList::Next</a> and  <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-item">IADsPropertyList::Item</a> respectively.


```cpp
IADsPropertyList *GetPropertyCache(LPWSTR);
IADsPropertyEntry *GetNextEntry(IADsPropertyList *);
IADsPropertyEntry *PropertyItem(IADsPropertyList *,LPWSTR);
 
void ResetItem(IADsPropertyList *pList, LPWSTR item)
{
    VARIANT var;
    VariantInit(&var);

    if(!pList)
    {
        item = NULL;
        return;
    }

    V_BSTR(&var)=SysAllocString(item);
    V_VT(&var)=VT_BSTR;
 
    pList->ResetPropertyItem(var);
    VariantClear(&var);
}
 
void TestResetItem()
{
    IADsPropertyEntry *pEntry = NULL;
    IADsPropertyList *pList = NULL;
    long count;
    BSTR bstr;
    HRESULT hr;
 
    pList = GetPropertyCache(L"WinNT://myComputer,computer");
 
    hr = pList->get_PropertyCount(&count);
    if(SUCCEEDED(hr))
    {
        printf(" Count before item reset : %d\n",count);
    }
 
    printf("Walking up the property list before item reset: \n");
    for (int i=0; i<count; i++)
    {
        pEntry = GetNextEntry(pList);
        hr = pEntry->get_Name(&bstr);
        if(SUCCEEDED(hr))
        {
            printf("   Name : %S\n",bstr);
            SysFreeString(bstr);
        }
    }
 
    pList->Reset();   // Move the cursor to the beginning of the list.
 
    ResetItem(pList, L"Owner");
 
    hr = pList->get_PropertyCount(&count);
    if(SUCCEEDED(hr))
    {
        printf(" Count after item reset : %d\n",count);
    }
 
    printf("Walking up the property list after item reset: \n");
 
    for (i=0; i<count; i++)
    {
        pEntry = GetNextEntry(pList);
        hr = pEntry->get_Name(&bstr);
        if(SUCCEEDED(hr))
        {
            printf("   Name : %S\n",bstr);
            SysFreeString(bstr);
        }
    }
 
    pEntry->Release();
    pList->Release();
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-item">IADsPropertyList::Item</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-next">IADsPropertyList::Next</a>