---
UID: NF:iads.IADsAccessControlList.AddAce
title: IADsAccessControlList::AddAce (iads.h)
description: The IADsAccessControlList::AddAce method adds an IADsAccessControlEntry object to the IADsAccessControlList object.
helpviewer_keywords: ["AddAce","AddAce method [ADSI]","AddAce method [ADSI]","IADsAccessControlList interface","IADsAccessControlList interface [ADSI]","AddAce method","IADsAccessControlList.AddAce","IADsAccessControlList::AddAce","_ds_iadsaccesscontrollist_addace","adsi.iadsaccesscontrollist__addace","adsi.iadsaccesscontrollist_addace","iads/IADsAccessControlList::AddAce"]
old-location: adsi\iadsaccesscontrollist_addace.htm
tech.root: adsi
ms.assetid: 663be55a-29d6-4a8a-adf2-024762413fc3
ms.date: 12/05/2018
ms.keywords: AddAce, AddAce method [ADSI], AddAce method [ADSI],IADsAccessControlList interface, IADsAccessControlList interface [ADSI],AddAce method, IADsAccessControlList.AddAce, IADsAccessControlList::AddAce, _ds_iadsaccesscontrollist_addace, adsi.iadsaccesscontrollist__addace, adsi.iadsaccesscontrollist_addace, iads/IADsAccessControlList::AddAce
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
 - IADsAccessControlList::AddAce
 - iads/IADsAccessControlList::AddAce
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
 - IADsAccessControlList.AddAce
---

# IADsAccessControlList::AddAce


## -description

   The <b>IADsAccessControlList::AddAce</b> method adds an <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a> object to the <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a> object.

## -parameters

### -param pAccessControlEntry [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface of the <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a> object to be added. This parameter cannot be <b>NULL</b>.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -remarks

Access control entries must appear in the following order in a security descriptor's access control list:

<ul>
<li>Access-denied ACEs that apply to the object itself</li>
<li>Access-denied ACEs that apply to a child of the object, such as a property set or property</li>
<li>Access-allowed ACEs that apply to the object itself</li>
<li>Access-allowed ACEs that apply to a child of the object, such as a property set or property</li>
<li>All inherited ACEs</li>
</ul>
This method adds the ACE to the front of the ACL, which does not necessarily result in correct ordering.


#### Examples

The following Visual Basic code example shows how to use the <b>IADsAccessControlList::AddAce</b> method to add two ACEs to an ACL.


```vb
Const ACL_REVISION_DS = &H4

Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim Ace1 As new IADsAccessControlEntry
Dim Ace2 As new IADsAccessControlEntry
Dim Dacl As new IADsAccessControlList
On Error GoTo Cleanup

Set x = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")

' Add the ACEs to the Discretionary ACL.
 
Dacl.AclRevision = ACL_REVISION_DS 'DS ACL Revision
' Set up the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "myMachine\Administrator"
 
' Set up the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "aDomain\aUser"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2

'Commit the changes. 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set Dacl = Nothing
    Set x = Nothing
    Set sd = Nothing

```


The following C++ code example adds an ACE to an ACL using the <b>IADsAccessControlList::AddAce</b> method. The added ACE has allowed access rights with the full permission.


```cpp
HRESULT addAceTo(IADsAccessControlList *pAcl)
{
    if(!pAcl) 
    {
        return E_FAIL;
    }

    HRESULT hr = pAcl->put_AclRevision(ACL_REVISION_DS);
    if(FAILED(hr)) 
    {
        return hr;
    }

    IADsAccessControlEntry *pAce = NULL; 
    pAce = createAce(-1,                    // Full permissions.
                     ADS_ACETYPE_ACCESS_ALLOWED,
                     ADS_ACEFLAG_INHERIT_ACE,
                     CComBSTR("aDomain\\aUser"));

    if(!pAce)
    {
        return E_FAIL;
    }

    IDispatch *pDisp;
    hr = pAce->QueryInterface(IID_IDispatch,(void**)&pDisp);
    if(FAILED(hr)) 
    {
        pAce->Release();
        return hr;
    }

    hr = pAcl->AddAce(pDisp);
    pDisp->Release();
    if(pAce) pAce->Release();
    if(FAILED(hr)) 
    {
        return hr;
    }

    printf("Ace has been added to ACL.\n");

    return hr;
}

////////////////////////////////////
// function to create an allowed ACE
////////////////////////////////////
IADsAccessControlEntry *createAce(
                   long mask,
                   long type, 
                   long flag,
                   BSTR trustee)
{
    HRESULT hr;
    IADsAccessControlEntry *pAce;
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pAce);
    if(FAILED(hr)) 
    {
        if(pAce) 
        {
            pAce->Release();
        }

        return NULL;
    }

    hr = pAce->put_AccessMask(mask); 
    hr = pAce->put_AceType(type);
    hr = pAce->put_AceFlags(flag);
    hr = pAce->put_Trustee(trustee); 

    return pAce;
}
```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IADsAccessControlList</a>