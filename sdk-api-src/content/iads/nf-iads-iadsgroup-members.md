---
UID: NF:iads.IADsGroup.Members
title: IADsGroup::Members (iads.h)
description: Retrieves a collection of the immediate members of the group.
helpviewer_keywords: ["IADsGroup interface [ADSI]","Members method","IADsGroup.Members","IADsGroup::Members","Members","Members method [ADSI]","Members method [ADSI]","IADsGroup interface","_ds_iadsgroup_members","adsi.iadsgroup__members","adsi.iadsgroup_members","iads/IADsGroup::Members"]
old-location: adsi\iadsgroup_members.htm
tech.root: adsi
ms.assetid: c909f779-ee27-4eb3-aee2-892ccc2a196e
ms.date: 12/05/2018
ms.keywords: IADsGroup interface [ADSI],Members method, IADsGroup.Members, IADsGroup::Members, Members, Members method [ADSI], Members method [ADSI],IADsGroup interface, _ds_iadsgroup_members, adsi.iadsgroup__members, adsi.iadsgroup_members, iads/IADsGroup::Members
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
 - IADsGroup::Members
 - iads/IADsGroup::Members
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
 - IADsGroup.Members
---

# IADsGroup::Members


## -description

The <b>IADsGroup::Members</b> method retrieves a collection of the immediate members of the group.  The collection does not include the members of other groups that are nested within the group.

The default implementation of this method uses <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a> to query name information for the group members. LsaLookupSids has a maximum limitation of 20480 SIDs it can convert, therefore that limitation also applies to this method.

## -parameters

### -param ppMembers [out]

Pointer to an <a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a> interface pointer that receives the collection of group members. The caller must  release this interface when it is no longer required.

## -returns

This method supports the standard return values, including <b>S_OK</b>. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The <a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a><b>Members</b> method will use the same provider.


#### Examples

The following code example enumerates all members of a group.


```vb
Dim grp As IADsGroup
Dim memberList As IADsMembers
Dim member As IADs

On Error GoTo Cleanup
 
Set grp = GetObject("WinNT://Microsoft/Administrators")
Set memberList = grp.Members
For Each m In memberList
    Set member = m
    Debug.Print member.Name & "(" & member.Class & ")"
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
    Set member = Nothing
    Set memberList = Nothing
```


The following code example enumerates all members of a group.


```cpp
HRESULT EnumerateGroupMembers(IADsGroup *pGroup)
{
    IADsMembers *pMembers;
    HRESULT hr = S_OK;
    hr = pGroup->Members(&pMembers);
    if(FAILED(hr)){goto Cleanup;}
 
    hr = EnumMembers(pMembers);  // For more information and a code
                                    example, see IADsMembers::get__NewEnum.
    if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pMembers)
        pMembers->Release();

    return hr;
}
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsgroup">IADsGroup</a>



<a href="/windows/desktop/ADSI/iadsgroup-property-methods">IADsGroup Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsmembers">IADsMembers</a>