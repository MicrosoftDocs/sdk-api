---
UID: NF:iads.IADsCollection.get__NewEnum
title: IADsCollection::get__NewEnum (iads.h)
description: The IADsCollection::get__NewEnum method gets a dependent enumerator object that implements IEnumVARIANT for this ADSI collection object. Be aware that there are two underscore characters in the function name (get__NewEnum).
helpviewer_keywords: ["IADsCollection interface [ADSI]","get__NewEnum method","IADsCollection.get__NewEnum","IADsCollection::get__NewEnum","_ds_iadscollection_get__newenum","adsi.iadscollection__get____newenum","adsi.iadscollection_get__newenum","get__NewEnum","get__NewEnum method [ADSI]","get__NewEnum method [ADSI]","IADsCollection interface","iads/IADsCollection::get__NewEnum"]
old-location: adsi\iadscollection_get__newenum.htm
tech.root: adsi
ms.assetid: db2630d0-26be-4cf1-811e-fc1d2007dda5
ms.date: 12/05/2018
ms.keywords: IADsCollection interface [ADSI],get__NewEnum method, IADsCollection.get__NewEnum, IADsCollection::get__NewEnum, _ds_iadscollection_get__newenum, adsi.iadscollection__get____newenum, adsi.iadscollection_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsCollection interface, iads/IADsCollection::get__NewEnum
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
 - IADsCollection::get__NewEnum
 - iads/IADsCollection::get__NewEnum
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
 - IADsCollection.get__NewEnum
---

# IADsCollection::get__NewEnum


## -description

The <b>IADsCollection::get__NewEnum</b> method gets a dependent enumerator object that implements  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> for this ADSI collection object. Be aware that there are two underscore characters in the function name (<b>get__NewEnum</b>).

## -parameters

### -param ppEnumerator [out]

Pointer to a pointer to the  <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the enumerator object for this collection.

## -returns

This method supports the standard return values including <b>S_OK</b>, <b>E_FAIL</b>, or <b>E_NOTIMPL</b>. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

When a server supports paged search and the client has specified the page limit greater than the maximum search results allowed on the server, the <b>IADsCollection::get__NewEnum</b> method returns errors in the following ways:

<ul>
<li>If the server returns an error with no results, the function returns the error only.</li>
<li>If the server returns partial results with or without an error, for example, the maximum search results allowed on the server, the function returns the partial results from the server to the user.</li>
<li>If the server returns all results with or without an error, for example, maximum search results on each page and all results through multiple pages, the function returns all the results from the server to the user.</li>
</ul>

#### Examples

The <b>For Each</b>…<b>In</b>…<b>Next</b> statement in the following Visual Basic code example invokes <b>get__NewEnum</b> method implicitly.


```vb
Dim fso As IADsFileServiceOperations 
On Error GoTo Cleanup

Set fso = GetObject("WinNT://myComputer/Fabrikam01") 
 
Dim coll As IADsCollection
Set coll = fso.Sessions
 
' The following statement invokes IADsCollection::get__NewEnum.
For Each session In coll 
   MsgBox "Session name: " & session.Name
Next session

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred... " & Err.Number)
    End If
    Set fso = Nothing
```


The following C++ code example shows how <b>IADsCollection::get__NewEnum</b> is used to enumerate active file service sessions.


```cpp
HRESULT EnumCollection(IADsCollection *);

HRESULT GetACollectionOfSessions()
{
    LPWSTR adspath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;

    // Bind to file service operations.
    IADsFileServiceOperations *pFso = NULL;
    hr = ADsGetObject(adspath,
                      IID_IADsFileServiceOperations,
                      (void**)&pFso);
    if(FAILED(hr)) {goto Cleanup;}

    // Get the pointer to the collection.
    hr = pFso->Sessions(&pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = EnumCollection(pColl);

Cleanup:
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();

    return hr;
}

HRESULT EnumCollection(IADsCollection *pColl)
{
    IUnknown *pUnk=NULL;
    HRESULT hr = S_OK;
    // Get the Enumerator object on the collection object.
    hr = pColl->get__NewEnum(&pUnk);
    if(FAILED(hr)) {goto Cleanup;}

    IEnumVARIANT *pEnum;
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    if(FAILED(hr)) {goto Cleanup;}

    // Enumerate the collection.
    BSTR bstr = NULL;
    VARIANT var;
    IADs *pADs = NULL;
    ULONG lFetch;
    IDispatch *pDisp = NULL;

    VariantInit(&var);
    hr = pEnum->Next(1, &var, &lFetch);
    while(hr == S_OK)
    {
        if (lFetch == 1)    
        {
             pDisp = V_DISPATCH(&var);
             pDisp->QueryInterface(IID_IADs, (void**)&pADs);
             pADs->get_Name(&bstr);
             printf("Session name: %S\n",bstr);
             SysFreeString(bstr);
             pADs->Release();
        }
        VariantClear(&var);
        pDisp->Release();
        pDisp = NULL;
        hr = pEnum->Next(1, &var, &lFetch);
    };
    

Cleanup:
    if(pDisp) pDisp->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pEnum) pEnum->Release();
    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>