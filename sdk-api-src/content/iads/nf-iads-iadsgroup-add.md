---
UID: NF:iads.IADsGroup.Add
title: IADsGroup::Add (iads.h)
description: Adds an ADSI object to an existing group.
helpviewer_keywords: ["Add","Add method [ADSI]","Add method [ADSI]","IADsGroup interface","IADsGroup interface [ADSI]","Add method","IADsGroup.Add","IADsGroup::Add","_ds_iadsgroup_add","adsi.iadsgroup__add","adsi.iadsgroup_add","iads/IADsGroup::Add"]
old-location: adsi\iadsgroup_add.htm
tech.root: adsi
ms.assetid: 7b660c3b-f395-407e-bc84-7ef7117298bb
ms.date: 12/05/2018
ms.keywords: Add, Add method [ADSI], Add method [ADSI],IADsGroup interface, IADsGroup interface [ADSI],Add method, IADsGroup.Add, IADsGroup::Add, _ds_iadsgroup_add, adsi.iadsgroup__add, adsi.iadsgroup_add, iads/IADsGroup::Add
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
 - IADsGroup::Add
 - iads/IADsGroup::Add
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
 - IADsGroup.Add
---

# IADsGroup::Add


## -description

The <b>IADsGroup::Add</b> method adds an ADSI object to an existing group.

## -parameters

### -param bstrNewItem [in]

Contains a <b>BSTR</b> that specifies the ADsPath of the object to add to the group. For more information, see Remarks.

## -returns

The following are the most common return values. For more information about return values, see <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

If the LDAP provider is used to bind to the <a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a> object, the same form of ADsPath must be specified in the <i>bstrNewItem</i> parameter. For example, if the ADsPath used to bind to the <b>IADsGroup</b> object includes a server, the ADsPath in the <i>bstrNewItem</i> parameter must contain the same server prefix. Likewise, if a serverless path is used to bind to the <b>IADsGroup</b> object, the <i>bstrNewItem</i> parameter must also contain a serverless path. When using server prefix, delays may occur if the group and the new member are from different domains, as requests may be sent to the wrong domain controller and referred to a domain controller of the correct domain and retried there. An exception occurs when adding or removing a member using a GUID or security identifier (SID) ADsPath. In this case, a serverless path should always be used in <i>bstrNewItem</i>.

The LDAP provider for Active Directory enables a member to be added to a group using the string form of the member SID. The <i>bstrNewItem</i> parameter can contain a SID string in the following form.


```cpp
LDAP://SID=<010500000000000515000000c6bb507afbda8b7f43170a325b040000>
```


For more information about SID strings in Active Directory, see <a href="/windows/desktop/AD/binding-to-an-object-using-a-sid">Binding to an Object Using a SID</a>.

The WinNT provider for Active Directory also enables a member to be added to a group using the string form of the member's SID. The <i>bstrNewItem</i> parameter can contain a SID string in the following form.


```cpp
WinNT://S-1-5-21-35135249072896"
```



#### Examples

The following code example shows how to add a user object ("jeff") to the group ("Administrators") on the "Fabrikam" domain, using the WinNT provider.


```vb
Dim grp As IADsGroup
Set grp = GetObject("WinNT://Fabrikam/Administrators")
grp.Add ("WinNT://Fabrikam/jeff")
```


The following code example shows how to add a user object to a group using the LDAP provider.


```vb
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("LDAP://CN=Administrators, CN=Users, DC=Fabrikam, DC=com")
grp.Add("LDAP://CN=Jeff Smith, OU=Sales,DC=Fabrikam,DC=com")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```


The following code example adds an existing user account to the Administrators group.


```cpp
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://Fabrikam/Administrators";
hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)) {goto Cleanup;}

// This assumes that the "WinNT://Fabrikam/jeff" user account exists 
// and does not already belong to the Administrators group.

hr = pGroup->Add(_bstr_t("WinNT://Fabrikam/jeff"));
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup)
        pGroup->Release();

    return hr;
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/AD/binding-to-an-object-using-a-sid">Binding to an Object Using a SID</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>



<a href="/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>