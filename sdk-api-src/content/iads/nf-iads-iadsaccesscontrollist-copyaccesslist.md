---
UID: NF:iads.IADsAccessControlList.CopyAccessList
title: IADsAccessControlList::CopyAccessList (iads.h)
description: The IADsAccessControlList::CopyAccessList method copies every access control entry (ACE) in the access-control list (ACL) to the caller's process space.
helpviewer_keywords: ["CopyAccessList","CopyAccessList method [ADSI]","CopyAccessList method [ADSI]","IADsAccessControlList interface","IADsAccessControlList interface [ADSI]","CopyAccessList method","IADsAccessControlList.CopyAccessList","IADsAccessControlList::CopyAccessList","_ds_iadsaccesscontrollist_copyaccesslist","adsi.iadsaccesscontrollist__copyaccesslist","adsi.iadsaccesscontrollist_copyaccesslist","iads/IADsAccessControlList::CopyAccessList"]
old-location: adsi\iadsaccesscontrollist_copyaccesslist.htm
tech.root: adsi
ms.assetid: 3f4c89ec-1144-4886-981a-75353d2dfe8b
ms.date: 12/05/2018
ms.keywords: CopyAccessList, CopyAccessList method [ADSI], CopyAccessList method [ADSI],IADsAccessControlList interface, IADsAccessControlList interface [ADSI],CopyAccessList method, IADsAccessControlList.CopyAccessList, IADsAccessControlList::CopyAccessList, _ds_iadsaccesscontrollist_copyaccesslist, adsi.iadsaccesscontrollist__copyaccesslist, adsi.iadsaccesscontrollist_copyaccesslist, iads/IADsAccessControlList::CopyAccessList
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
 - IADsAccessControlList::CopyAccessList
 - iads/IADsAccessControlList::CopyAccessList
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
 - IADsAccessControlList.CopyAccessList
---

# IADsAccessControlList::CopyAccessList


## -description

The <b>IADsAccessControlList::CopyAccessList</b> method copies every access control entry (ACE) in the access-control list (ACL) to the caller's process space.

## -parameters

### -param ppAccessControlList [out]

Address of an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to an ACL as the copy of the original access list. If this parameter is <b>NULL</b> on return, no copies of the ACL could be made.

## -returns

This method returns the standard return values.

For more information about  other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The caller must call <b>Release</b> on the copy of ACEs through their <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointers.


#### Examples

The following code example shows how to copy an ACL from one ADSI object to another.


```vb
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim Dacl As IADsAccessControlList
Dim CopyDacl As IADsAccessControlList
 
' Get the ACL from one object.
Set x = GetObject("LDAP://OU=Sales, DC=activeD,DC=mydomain,DC=fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
Set CopyDacl = Dacl.CopyAccessList()
 
' Copy the ACL to another object in the Directory.
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
sd.DiscretionaryAcl = CopyDacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set sd = Nothing
    Set Dacl = Nothing
    Set CopyDacl = Nothing

```


The following code example copies the ACL from the source object to the target object.


```cpp
HRESULT CopyACL(IADs *pSource, IADs *pTarget)
{
    IADsSecurityDescriptor *pSourceSD = NULL;
    IADsSecurityDescriptor *pTargetSD = NULL;    
    IDispatch *pDisp = NULL;
    
    HRESULT hr = S_OK;
    VARIANT varSource, varTarget;
    
    VariantInit(&varSource);
    VariantInit(&varTarget);

    if((pSource==NULL) || (pTarget==NULL))
    {
        return E_FAIL;
    }
    
    hr = pSource->Get(CComBSTR("ntSecurityDescriptor"), &varSource);
    if(FAILED(hr))
    {
        goto Cleanup;
    }
    
    hr = pTarget->Get(CComBSTR("ntSecurityDescriptor"), &varTarget);
    if(FAILED(hr))
    {
        goto Cleanup;
    }
    
    hr = V_DISPATCH(&varSource)->QueryInterface(IID_IADsSecurityDescriptor,
                    (void**)&pSourceSD);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    

    hr = V_DISPATCH(&varTarget)->QueryInterface(IID_IADsSecurityDescriptor,
                    (void**)&pTargetSD);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    
    
    hr = pSourceSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    

    hr = pTargetSD->put_DiscretionaryAcl(pDisp);
    if(FAILED(hr))
    {
        goto Cleanup;
    }    
    
    hr = pTarget->SetInfo();
        
Cleanup:
    VariantClear(&varSource);
    VariantClear(&varTarget);
    if(pSourceSD) 
    {
        pSourceSD->Release();
    }
    if(pTargetSD) 
    {
        pTargetSD->Release();
    }
    if(pDisp) 
    {
        pDisp->Release();
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>