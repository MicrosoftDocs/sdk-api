---
UID: NF:iads.IADsCollection.Remove
title: IADsCollection::Remove (iads.h)
description: The IADsCollection::Remove method removes the named item from this ADSI collection object.
helpviewer_keywords: ["IADsCollection interface [ADSI]","Remove method","IADsCollection.Remove","IADsCollection::Remove","Remove","Remove method [ADSI]","Remove method [ADSI]","IADsCollection interface","_ds_iadscollection_remove","adsi.iadscollection__remove","adsi.iadscollection_remove","iads/IADsCollection::Remove"]
old-location: adsi\iadscollection_remove.htm
tech.root: adsi
ms.assetid: 21ce80fe-542b-4350-b66c-fa26f62ca611
ms.date: 12/05/2018
ms.keywords: IADsCollection interface [ADSI],Remove method, IADsCollection.Remove, IADsCollection::Remove, Remove, Remove method [ADSI], Remove method [ADSI],IADsCollection interface, _ds_iadscollection_remove, adsi.iadscollection__remove, adsi.iadscollection_remove, iads/IADsCollection::Remove
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
 - IADsCollection::Remove
 - iads/IADsCollection::Remove
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
 - IADsCollection.Remove
---

# IADsCollection::Remove


## -description

The <b>IADsCollection::Remove</b> method removes the named item from this ADSI collection object.

## -parameters

### -param bstrItemToBeRemoved [in]

The null-terminated Unicode string that specifies the name of the item as it was specified by  <a href="/windows/desktop/api/iads/nf-iads-iadscollection-add">IADsCollection::Add</a>.

## -returns

This method supports the standard return values, including <b>S_OK</b>. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

Collections for a directory service can also consist of a set of immutable objects.

Collections that do not support direct removal of items are required to return <b>E_NOTIMPL</b>.


#### Examples

The following Visual Basic code example shows how to remove a named session object from a collection of active file service sessions.


```vb
Dim fso As IADsFileServiceOperations 
Dim ses As IADsSession
Dim coll As IADsCollection
Dim mySessionName As String

On Error GoTo Cleanup

Set fso = GetObject("WinNT://myComputer/FabrikamServer") 
Set coll = fso.Sessions

' Insert code to set mySessionName to the name of the mySession 
' session object.
 
' The following statement invokes IADsCollection::Remove.
coll.Remove mySessionName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
    Set ses = Nothing
    Set coll = Nothing

```


The following C++ code example shows how to remove a named session object from a collection of active file service sessions.


```cpp
HRESULT RemoveASessionObjectFromCollection()
{
    LPWSTR adspath = L"WinNT://myComputer/FabrikamServer";
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;
    IADsFileServiceOperations *pFso = NULL;

    hr = ADsGetObject(adspath,IID_IADsFileServiceOperations,(void**)&pFso);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFso->Sessions(&pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pColl->Remove(CComBSTR("MySession"));

Cleanup
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();

    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscollection-add">IADsCollection::Add</a>