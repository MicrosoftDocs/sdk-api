---
UID: NF:iads.IADsAccessControlList.AddAce
title: IADsAccessControlList::AddAce
author: windows-sdk-content
description: The IADsAccessControlList::AddAce method adds an IADsAccessControlEntry object to the IADsAccessControlList object.
old-location: adsi\iadsaccesscontrollist_addace.htm
old-project: ADSI
ms.assetid: 663be55a-29d6-4a8a-adf2-024762413fc3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AddAce, AddAce method [ADSI], AddAce method [ADSI],IADsAccessControlList interface, IADsAccessControlList interface [ADSI],AddAce method, IADsAccessControlList.AddAce, IADsAccessControlList::AddAce, _ds_iadsaccesscontrollist_addace, adsi.iadsaccesscontrollist__addace, adsi.iadsaccesscontrollist_addace, iads/IADsAccessControlList::AddAce
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
 - IADsAccessControlList.AddAce
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsAccessControlList::AddAce


## -description


   The <b>IADsAccessControlList::AddAce</b> method adds an <a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a> object to the <a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a> object.


## -parameters




### -param pAccessControlEntry [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface of the <a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a> object to be added. This parameter cannot be <b>NULL</b>.


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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const ACL_REVISION_DS = &amp;H4

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
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set Dacl = Nothing
    Set x = Nothing
    Set sd = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following C++ code example adds an ACE to an ACL using the <b>IADsAccessControlList::AddAce</b> method. The added ACE has allowed access rights with the full permission.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT addAceTo(IADsAccessControlList *pAcl)
{
    if(!pAcl) 
    {
        return E_FAIL;
    }

    HRESULT hr = pAcl-&gt;put_AclRevision(ACL_REVISION_DS);
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
    hr = pAce-&gt;QueryInterface(IID_IDispatch,(void**)&amp;pDisp);
    if(FAILED(hr)) 
    {
        pAce-&gt;Release();
        return hr;
    }

    hr = pAcl-&gt;AddAce(pDisp);
    pDisp-&gt;Release();
    if(pAce) pAce-&gt;Release();
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
                          (void**)&amp;pAce);
    if(FAILED(hr)) 
    {
        if(pAce) 
        {
            pAce-&gt;Release();
        }

        return NULL;
    }

    hr = pAce-&gt;put_AccessMask(mask); 
    hr = pAce-&gt;put_AceType(type);
    hr = pAce-&gt;put_AceFlags(flag);
    hr = pAce-&gt;put_Trustee(trustee); 

    return pAce;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6d2cd45b-0dc6-4bb3-9c41-014bec71f258">IADsAccessControlEntry</a>



<a href="https://msdn.microsoft.com/de92d9cc-bc9d-4dc5-aa79-01f4d3050c35">IADsAccessControlList</a>
 

 

