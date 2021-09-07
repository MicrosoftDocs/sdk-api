---
UID: NN:iads.IADsAccessControlList
title: IADsAccessControlList (iads.h)
description: The IADsAccessControlList interface is a dual interface that manages individual access-control entries (ACEs).
helpviewer_keywords: ["AccessControlList","IADsAccessControlList","IADsAccessControlList interface [ADSI]","IADsAccessControlList interface [ADSI]","described","_ds_iadsaccesscontrollist","adsi.iadsaccesscontrollist","iads/IADsAccessControlList"]
old-location: adsi\iadsaccesscontrollist.htm
tech.root: adsi
ms.assetid: de92d9cc-bc9d-4dc5-aa79-01f4d3050c35
ms.date: 12/05/2018
ms.keywords: AccessControlList, IADsAccessControlList, IADsAccessControlList interface [ADSI], IADsAccessControlList interface [ADSI],described, _ds_iadsaccesscontrollist, adsi.iadsaccesscontrollist, iads/IADsAccessControlList
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
 - IADsAccessControlList
 - iads/IADsAccessControlList
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
 - IADsAccessControlList
 - AccessControlList
---

# IADsAccessControlList interface


## -description

The <b>IADsAccessControlList</b> interface is a dual interface that manages individual access-control entries (ACEs).

## -inheritance

The <b>IADsAccessControlList</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsAccessControlList</b> also has these types of members:

## -remarks

An access-control list (ACL) is a collection of ACEs that can provide more specific access control to the same ADSI object for different clients. In general, different providers implement different access controls and therefore the behavior of the object is specific to the provider.  For more information, see  the provider documentation. For more information about Microsoft providers, see  <a href="/windows/desktop/ADSI/adsi-system-providers">ADSI System Providers</a>. Currently, only the LDAP provider supports access controls.

Before you can work with an object ACE, first obtain the ACL to which they belong. ACLs are managed by security descriptors and can be of either discretionary ACL and system ACL. For more information, see 
  <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>.

Using the properties and methods of the <b>IADsAccessControlList</b> interface, you can retrieve and enumerate ACEs, add new entries to the list, or remove existing entries.

<p class="proch"><b>To manage access controls over an ADSI</b>

<ol>
<li>First, retrieve the security descriptor of the object that implements the  <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface.</li>
<li>Second, retrieve the ACL from the security descriptor.</li>
<li>Third, work with the ACE, or ACEs, of the object in the ACL.</li>
</ol>
<p class="proch"><b>To make any new or modified ACEs persistent</b>

<ol>
<li>First, add the ACE to the ACL.</li>
<li>Second, assign the ACL to the security descriptor.</li>
<li>Third, commit the security descriptor to the directory store.</li>
</ol>
For more information about DACLs, see <a href="/windows/desktop/AD/null-dacls-and-empty-dacls">Null DACLs and Empty DACLs</a>.


#### Examples

The following code example shows  how to work with access control entries of a discretionary ACL.


```vb
Dim X As IADs
Dim Namespace As IADsOpenDSObject
Dim SecurityDescriptor As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList

On Error GoTo Cleanup
 
Set Namespace = GetObject("LDAP://")
Set X= Namespace.OpenDSObject("LDAP://DC=Fabrikam,DC=Com, vbNullString, vbNullString,  ADS_SECURE_AUTHENTICATION)
 
Set SecurityDescriptor = X.Get("ntSecurityDescriptor")
Debug.Print SecurityDescriptor.Owner
Debug.Print SecurityDescriptor.Group
 
Set Dacl = SecurityDescriptor.DiscretionaryAcl
Debug.Print Dacl.AceCount
 
For Each Obj In Dacl
   Debug.Print Obj.Trustee
   Debug.Print Obj.AccessMask
   Debug.Print Obj.AceFlags
   Debug.Print Obj.AceType
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set X = Nothing
    Set Namespace = Nothing
    Set SecurityDescriptor = Nothing
    Set Dacl = Nothing
```


The following code example enumerates ACEs from a DACL.


```cpp
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"), &var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/AD/null-dacls-and-empty-dacls">Null DACLs and Empty DACLs</a>
