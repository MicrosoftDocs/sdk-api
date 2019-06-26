---
UID: NF:iads.IADsCollection.GetObject
title: IADsCollection::GetObject (iads.h)
author: windows-sdk-content
description: Retrieves an item of the collection.
old-location: adsi\iadscollection_getobject.htm
tech.root: adsi
ms.assetid: 04b33451-505e-43de-8db4-3e37f9909ea6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [ADSI], GetObject method [ADSI],IADsCollection interface, IADsCollection interface [ADSI],GetObject method, IADsCollection.GetObject, IADsCollection::GetObject, _ds_iadscollection_getobject, adsi.iadscollection__getobject, adsi.iadscollection_getobject, iads/IADsCollection::GetObject
ms.topic: method
f1_keywords: 
 - "iads/IADsCollection.GetObject"
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
 - IADsCollection.GetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsCollection::GetObject


## -description


The <b>IADsCollection::GetObject</b> method retrieves an item of the collection.


## -parameters




### -param bstrName [in]

The null-terminated Unicode string that specifies the name of the item. This is the same name passed to  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscollection-add">IADsCollection::Add</a> when the item is added to the collection.


### -param pvItem [in]

Current value of the item. For an object, this corresponds to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer on the object.


## -returns



This method supports the standard return values, including S_OK. For more information and other return values, see  <a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.




## -remarks



If you know the name of a session in the <b>Sessions</b> collection, call the <b>IADsCollection::GetObject</b> method explicitly to retrieve the session object.


#### Examples

The following Visual Basic code example shows how to retrieve a named session object from a collection of active file service sessions.


```vb
Dim fso As IADsFileServiceOperations 
Dim ses As IADsSession
Dim coll As IADsCollection
Dim mySessionName As String

Set fso = GetObject("WinNT://myComputer/FabrikamServer") 
Set coll = fso.Sessions

' Insert code to set mySessionName to the name of mySession.
 
' The following statement invokes IADsCollection::GetObject.
Set ses = coll.GetObject(mySessionName)
```


The following C++ code example shows how to retrieve a named session object from a collection of active file service sessions.


```cpp
HRESULT GetASessionObjectFromCollection(BSTR mySession)
{
    LPWSTR adspath = L"WinNT://myComputer/FabrikamServer";
    IUnknown *pUnk=NULL;
    HRESULT hr = S_OK;
    IADsCollection *pColl = NULL;
    IADsFileServiceOperations *pFso = NULL;
    IADs *pADsObj = NULL;
    VARIANT varObj;
    BSTR bstrObj = NULL;

    VariantInit(&varObj);
    hr = ADsGetObject(adspath, 
                      IID_IADsFileServiceOperations,
                      (void**)&pFso);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFso->Sessions(&pColl);
    if(FAILED(hr)) {goto Cleanup;}

    hr = pColl->GetObject(mySession, &varObj);
    V_DISPATCH(&varObj)->QueryInterface(IID_IADs,(void**)&pADsObj);
    hr = pADsObj->get_Class(&bstrObj);
    printf("Class of the object obtained from GetObject: %S\n",
             bstrObj);

Cleanup:
    if(bstrObj) SysFreeString(bstrObj);
    if(pFso) pFso->Release();
    VariantClear(&varObj);
    if(pADsObj) pADsObj->Release();
    if(pColl) pColl->Release();

    return hr;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ADSI/adsi-error-codes">ADSI Error
  Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscollection-add">IADsCollection::Add</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>
 

 

