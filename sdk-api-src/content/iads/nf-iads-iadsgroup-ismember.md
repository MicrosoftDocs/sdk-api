---
UID: NF:iads.IADsGroup.IsMember
title: IADsGroup::IsMember
author: windows-sdk-content
description: Determines if a directory service object is an immediate member of the group.
old-location: adsi\iadsgroup_ismember.htm
old-project: ADSI
ms.assetid: 16251638-49c6-48f0-b398-0bf8f523ba86
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsGroup interface [ADSI],IsMember method, IADsGroup.IsMember, IADsGroup::IsMember, IsMember, IsMember method [ADSI], IsMember method [ADSI],IADsGroup interface, _ds_iadsgroup_ismember, adsi.iadsgroup__ismember, adsi.iadsgroup_ismember, iads/IADsGroup::IsMember
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsGroup.IsMember
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsGroup::IsMember


## -description


The <b>IADsGroup::IsMember</b> method determines if a directory service object is an immediate member of the group. This method does not verify membership in any nested groups.


## -parameters




### -param bstrMember

Contains the ADsPath of the directory service object to verify membership. This ADsPath must use the same ADSI provider used to bind to the group. For example, if the group was bound to using the LDAP provider, this ADsPath must also use the LDAP provider.


### -param bMember [out]

Pointer to a <b>VARIANT_BOOL</b> value that receives <b>VARIANT_TRUE</b> if the object is an immediate member of the group or <b>VARIANT_FALSE</b> otherwise.


## -returns



This method supports the standard return values, including <b>S_OK</b>. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Although you can add or remove a security principal to or from a group using the member SID through the WinNT provider, the <b>IADsGroup.IsMember</b> method does not support using a SID ADsPath for verification if a member belongs to a group through the WinNT provider.

The <b>IADsGroup::IsMember</b> method will only work correctly if the group and the object are in the same domain. If the object is in a different domain than the group, <b>IADsGroup::IsMember</b> will always return <b>VARIANT_FALSE</b>.


#### Examples

The following code example adds the "jeffsmith" user to the "Administrators" group on the "Fabrikam" domain and then reports that the user is now a member of the group.


```vb
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
grp.Add ("WinNT://Fabrikam/jeffsmith")
Debug.Print grp.IsMember("WinNT://Fabrikam/jeffsmith ") ' Should be TRUE.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```


The following code example verifies that a user belongs to a group before adding it to the group.


```cpp
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://Fabrikam/Administrators";
BSTR bstr = NULL;

hr = ADsGetObject(adsPath, IID_IADsGroup, (void**)&pGroup);

if(FAILED(hr))
{
    goto Cleanup;
}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr))
{
    goto Cleanup;
}

printf("Description: %S\n",bstr);
SysFreeString(bstr);

VARIANT_BOOL inG=false;
hr = pGroup->IsMember(CComBSTR("WinNT://Microsoft/SecUser"), &inG);

if (inG ) 
{
    printf("already in the group.\n");
}
else 
{
    hr = pGroup->Add(CComBSTR("WinNT://Microsoft/SecUser"));
    if(FAILED(hr))
    {
        goto Cleanup;
    }

    printf("user added.\n");
}

Cleanup:
if(pGroup)
{
    pGroup->Release();
}
if(bstr)
{
    SysFreeString(bstr);
}

return hr;
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup Property Methods</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>
 

 

