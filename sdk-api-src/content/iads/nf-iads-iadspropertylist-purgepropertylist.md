---
UID: NF:iads.IADsPropertyList.PurgePropertyList
title: IADsPropertyList::PurgePropertyList (iads.h)
description: Deletes all items from the property list.
helpviewer_keywords: ["IADsPropertyList interface [ADSI]","PurgePropertyList method","IADsPropertyList.PurgePropertyList","IADsPropertyList::PurgePropertyList","PurgePropertyList","PurgePropertyList method [ADSI]","PurgePropertyList method [ADSI]","IADsPropertyList interface","_ds_iadspropertylist_purgepropertylist","adsi.iadspropertylist__purgepropertylist","adsi.iadspropertylist_purgepropertylist","iads/IADsPropertyList::PurgePropertyList"]
old-location: adsi\iadspropertylist_purgepropertylist.htm
tech.root: adsi
ms.assetid: 872c8af7-60c4-4dfc-aa37-0cbb2229a93f
ms.date: 12/05/2018
ms.keywords: IADsPropertyList interface [ADSI],PurgePropertyList method, IADsPropertyList.PurgePropertyList, IADsPropertyList::PurgePropertyList, PurgePropertyList, PurgePropertyList method [ADSI], PurgePropertyList method [ADSI],IADsPropertyList interface, _ds_iadspropertylist_purgepropertylist, adsi.iadspropertylist__purgepropertylist, adsi.iadspropertylist_purgepropertylist, iads/IADsPropertyList::PurgePropertyList
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
 - IADsPropertyList::PurgePropertyList
 - iads/IADsPropertyList::PurgePropertyList
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
 - IADsPropertyList.PurgePropertyList
---

# IADsPropertyList::PurgePropertyList


## -description

The <b>IADsPropertyList::PurgePropertyList</b> method deletes all items from the property list.



## -returns

This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When the <b>PurgePropertyList</b> method is called, all the items are removed from the cache. Thus, calling  <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-getpropertyitem">GetPropertyItem</a> after that will generate an error. Be aware that <b>PurgePropertyList</b> only affects the contents of the cache and does not affect the properties on the actual object in the directory; that is, calling  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">SetInfo</a> after calling <b>PurgePropertyList</b> does not delete the properties on the directory object.


#### Examples

The following code example shows how to implement <b>IADsPropertyList::PurgePropertyList</b>.


```vb
Dim propList As IADsPropertyList
 
On Error GoTo Cleanup

Set propList = GetObject("LDAP://dc03/DC=Fabrikam,DC=com")
propList.GetInfo
 
propList.PurgePropertyList
 
'- None of GetPropertyItem should work, because the list is purged.
'- The following line should generate error.
Set propEntry = propList.GetPropertyItem("adminDescription", ADSTYPE_CASE_IGNORE_STRING)

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing

```


The following code example shows the effect produced by a call to <b>IADsPropertyList::PurgePropertyList</b>.  For more information about the <b>GetPropertyCache</b>  function and a code example, see <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>.


```cpp
IADsPropertyList *GetPropertyCache(LPWSTR);
 
void TestPurgePropertyList()
{
    IADsPropertyList *pList;
    pList=GetPropertyCache(L"WinNT://myComputer,computer");
 
    long count;

    if(pList)
    {
        pList->get_PropertyCount(&count);
        printf("Number of properties before purging: %d\n",count);
 
        count = -1;
        pList->PurgePropertyList();
        pList->get_PropertyCount(&count);
        printf("Number of properties after purging: %d\n",count);
    }
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-getpropertyitem">IADsPropertyList::GetPropertyItem</a>
