---
UID: NF:iads.IADsContainer.get__NewEnum
title: IADsContainer::get__NewEnum (iads.h)
description: Retrieves an enumerator object for the container.
helpviewer_keywords: ["IADsContainer interface [ADSI]","get__NewEnum method","IADsContainer.get__NewEnum","IADsContainer::get__NewEnum","_ds_iadscontainer_get__newenum","adsi.iadscontainer__get____newenum","adsi.iadscontainer_get__newenum","get__NewEnum","get__NewEnum method [ADSI]","get__NewEnum method [ADSI]","IADsContainer interface","iads/IADsContainer::get__NewEnum"]
old-location: adsi\iadscontainer_get__newenum.htm
tech.root: adsi
ms.assetid: b268efb8-59cd-41ef-b96c-583ae476432e
ms.date: 12/05/2018
ms.keywords: IADsContainer interface [ADSI],get__NewEnum method, IADsContainer.get__NewEnum, IADsContainer::get__NewEnum, _ds_iadscontainer_get__newenum, adsi.iadscontainer__get____newenum, adsi.iadscontainer_get__newenum, get__NewEnum, get__NewEnum method [ADSI], get__NewEnum method [ADSI],IADsContainer interface, iads/IADsContainer::get__NewEnum
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
 - IADsContainer::get__NewEnum
 - iads/IADsContainer::get__NewEnum
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
 - IADsContainer.get__NewEnum
---

# IADsContainer::get__NewEnum


## -description

The <b>IADsContainer::get__NewEnum</b> method Retrieves an enumerator object for the container. The 
  enumerator object implements the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface to enumerate the children of the container object.

## -parameters

### -param retval [out]

Pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer that receives the enumerator object. The caller must release this interface when it is no longer required.

## -returns

This method supports the standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

There are two underscore characters ("__") in the function name between "get" and "NewEnum".

In Visual Basic, use the <b>For</b><b>Each</b>… statement to invoke the <b>IADsContainer::get__NewEnum</b> method implicitly.

In C/C++, use the  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a>,  <a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>, and <a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">AdsFreeEnumerator</a> helper functions.


#### Examples

The following code example shows how to enumerate child objects in a container.


```vb
Dim cont As IADsContainer
On Error GoTo Cleanup

Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
For Each obj In cont
  Debug.Print obj.Name
Next

Cleanup:
    If(Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
```


The following code example shows how to enumerate the object contained in a container.


```cpp
IEnumVARIANT *pEnum = NULL;
IADsContainer *pCont = NULL;
LPUNKNOWN pUnk = NULL;
VARIANT var;
IDispatch *pDisp = NULL;
ulong lFetch;
IADs *pADs = NULL;
 
// In this sample, skip error checking.
ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM", 
                        IID_IADsContainer, (void**) &pCont);
pCont->get__NewEnum(&pUnk);
pCont->Release();
 
pUnk->QueryInterface(IID_IEnumVARIANT, (void**) &pEnum);
pUnk->Release();
 
// Enumerate. 
HRESULT hr = pEnum->Next(1, &var, &lFetch);
while(SUCCEEDED(hr) && lFetch > 0)
{
    if (lFetch == 1)
    {
        BSTR bstr;

        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADs, (void**)&pADs); 
        pDisp->Release();
        hr = pADs->get_Name(&bstr);
        if(SUCCEEDED(hr))
        {
            SysFreeString(bstr);
        }

        pADs->Release();
    }

    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

 
pEnum->Release();
```

## -see-also

<a href="/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator">ADsBuildEnumerator</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">AdsFreeEnumerator</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>