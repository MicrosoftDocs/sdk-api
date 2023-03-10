---
UID: NF:iads.IADsGroup.Remove
title: IADsGroup::Remove (iads.h)
description: The IADsGroup::Remove method removes the specified user object from this group. The operation does not remove the group object itself even when there is no member remaining in the group.
helpviewer_keywords: ["IADsGroup interface [ADSI]","Remove method","IADsGroup.Remove","IADsGroup::Remove","Remove","Remove method [ADSI]","Remove method [ADSI]","IADsGroup interface","_ds_iadsgroup_remove","adsi.iadsgroup__remove","adsi.iadsgroup_remove","iads/IADsGroup::Remove"]
old-location: adsi\iadsgroup_remove.htm
tech.root: adsi
ms.assetid: bf309f0a-1ef5-4123-91c5-ae232ddd6340
ms.date: 12/05/2018
ms.keywords: IADsGroup interface [ADSI],Remove method, IADsGroup.Remove, IADsGroup::Remove, Remove, Remove method [ADSI], Remove method [ADSI],IADsGroup interface, _ds_iadsgroup_remove, adsi.iadsgroup__remove, adsi.iadsgroup_remove, iads/IADsGroup::Remove
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
 - IADsGroup::Remove
 - iads/IADsGroup::Remove
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
 - IADsGroup.Remove
---

# IADsGroup::Remove


## -description

The <b>IADsGroup::Remove</b> method removes the specified user object from this group. The operation does not remove the group object itself even when there is no member remaining in the group.

## -parameters

### -param bstrItemToBeRemoved [in]

Contains a <b>BSTR</b> that specifies the ADsPath of the object to remove from the group. For more information about this parameter, see the Remarks section.

## -returns

The following are the most common return values. For more information about return values, see <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

If the LDAP provider is used to bind to the <a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a> object, the same form of ADsPath must be specified in the <i>bstrItemToBeRemoved</i> parameter. For example, if the ADsPath used to bind to the <b>IADsGroup</b> object includes a server, the ADsPath in the <i>bstrItemToBeRemoved</i> parameter must contain the same server prefix. Likewise, if a serverless path is used to bind to the <b>IADsGroup</b> object, the <i>bstrItemToBeRemoved</i> parameter must also contain a serverless path. The exception is when adding or removing a member using a GUID or SID ADsPath. In this case, a serverless path should always be used in <i>bstrItemToBeRemoved</i>.

You can use a SID in the ADsPath to remove a security principal from the group through the WinNT provider. For example, suppose the SID of a user, "Fabrikam\jeffsmith", is S-1-5-21-35135249072896, the following statement:


```vb
Dim group As IADsGroup
group.Remove("WinNT://S-1-5-21-35135249072896")
```


is equivalent to


```vb
Dim group As IADsGroup
group.Remove("WinNT://Fabrikam/jeffsmith")
```


Removing a member using its SID through the WinNT provider is a new feature in Windows 2000 and the DSCLIENT package.


#### Examples

The following code example removes a user account from a group.


```vb
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Fabrikam/Administrators")
grp.Remove ("WinNT://Fabrikam/jeffsmith")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```


The following code example removes a user from a group.


```cpp
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR usrPath = L"WinNT://Fabrikam/jeffsmith";
LPWSTR grpPath = L"WinNT://Fabrikam/Administrators";

hr = ADsGetObject(grpPath, IID_IADsGroup, (void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Remove(CComBSTR(usrPath));
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup)
        pGroup->Release();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>



<a href="/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>