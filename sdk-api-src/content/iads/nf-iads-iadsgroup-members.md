---
UID: NF:iads.IADsGroup.Members
title: IADsGroup::Members (iads.h)
author: windows-sdk-content
description: Retrieves a collection of the immediate members of the group.
old-location: adsi\iadsgroup_members.htm
tech.root: adsi
ms.assetid: c909f779-ee27-4eb3-aee2-892ccc2a196e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsGroup interface [ADSI],Members method, IADsGroup.Members, IADsGroup::Members, Members, Members method [ADSI], Members method [ADSI],IADsGroup interface, _ds_iadsgroup_members, adsi.iadsgroup__members, adsi.iadsgroup_members, iads/IADsGroup::Members
ms.topic: method
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
 - IADsGroup.Members
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsGroup::Members


## -description


The <b>IADsGroup::Members</b> method retrieves a collection of the immediate members of the group.  The collection does not include the members of other groups that are nested within the group.


## -parameters




### -param ppMembers [out]

Pointer to an <a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a> interface pointer that receives the collection of group members. The caller must  release this interface when it is no longer required.


## -returns



This method supports the standard return values, including <b>S_OK</b>. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a><b>Members</b> method will use the same provider.


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




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup Property Methods</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>
 

 

