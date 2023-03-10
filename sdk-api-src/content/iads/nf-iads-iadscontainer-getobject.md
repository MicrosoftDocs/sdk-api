---
UID: NF:iads.IADsContainer.GetObject
title: IADsContainer::GetObject (iads.h)
description: Retrieves an interface for a directory object in the container.
helpviewer_keywords: ["GetObject","GetObject method [ADSI]","GetObject method [ADSI]","IADsContainer interface","IADsContainer interface [ADSI]","GetObject method","IADsContainer.GetObject","IADsContainer::GetObject","_ds_iadscontainer_getobject","adsi.iadscontainer__getobject","adsi.iadscontainer_getobject","iads/IADsContainer::GetObject"]
old-location: adsi\iadscontainer_getobject.htm
tech.root: adsi
ms.assetid: df8b1eae-1138-4e55-af6e-17c6105ca9c1
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [ADSI], GetObject method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],GetObject method, IADsContainer.GetObject, IADsContainer::GetObject, _ds_iadscontainer_getobject, adsi.iadscontainer__getobject, adsi.iadscontainer_getobject, iads/IADsContainer::GetObject
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
 - IADsContainer::GetObject
 - iads/IADsContainer::GetObject
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
 - IADsContainer.GetObject
---

# IADsContainer::GetObject


## -description

The <b>IADsContainer::GetObject</b> method retrieves an 
interface for a directory object in the container.

## -parameters

### -param ClassName [in]

A <b>BSTR</b> that specifies the name of the object class as of the object to retrieve. If this parameter is <b>NULL</b>, the provider returns the first item found in the container.

### -param RelativeName [in]

A <b>BSTR</b> that specifies the relative distinguished name of the object to retrieve.

### -param ppObject [out]

A pointer to a pointer to the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface on the specified object.

## -returns

This method supports standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

For the LDAP provider, the <i>bstrRelativeName</i> parameter must contain the name prefix, such as "CN=Jeff Smith". The <i>bstrRelativeName</i> parameter can also contain more than one level of name, such as "CN=Jeff Smith,OU=Sales".

In C++, when <b>GetObject</b> has succeeded, the caller must query the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface for the desired interface using the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method.

The <i>bstrClassName</i> parameter can be either a valid class name or <b>NULL</b>. If the class name is not valid, including when it contains a blank space, this method will throw an <a href="/windows/desktop/ADSI/generic-adsi-error-codes">E_ADS_UNKNOWN_OBJECT</a> error.


#### Examples

The following code example  retrieves a user object from a container object.


```vb
Dim cont As IADsContainer
Dim usr As IADsUser
Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set usr = cont.GetObject("user", "CN=jeffsmith")
```


This is equivalent to:


```vb
Dim usr As IADsUser
Set usr=GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=com")
```


The following code example retrieves a user object from a container object.


```cpp
HRESULT hr = S_OK;
CoInitialize(NULL);
 
IADsContainer *pCont = NULL;
 
hr = ADsGetObject(L"LDAP://DC=windows2000,DC=mytest,DC=fabrikam,DC=com",
            IID_IADsContainer, 
            (void**) &pCont );

if(FAILED(hr))
{
    goto Cleanup;
}
 
///////////////////////////////////////////////////////////////////////
// Retrieve the child from the container.
// Be aware that in the LDAP provider you can navigate multiple levels.
///////////////////////////////////////////////////////////////////////
IDispatch *pDisp = NULL;
IADs *pADs = NULL;
hr = pCont->GetObject(CComBSTR("user"), CComBSTR("CN=Jeff Smith,OU=DSys"), &pDisp);
pCont->Release();
if(FAILED(hr))
{
    goto Cleanup;
}
 
hr = pDisp->QueryInterface(IID_IADs, (void**)&pADs);
pDisp->Release(); 
if(FAILED(hr))
{
    goto Cleanup;
}
 
// Perform an operation with pADs.
pADs->Release();
 
Cleanup:
if(pCont)
    pCont->Release();

if(pDisp)
    pDisp->Release();

if(pADs)
    pADs->Release();

CoUninitialize();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error
  Codes</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a>



<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<b>IADs::get_Class</b>



<b>IADs::get_Name</b>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>