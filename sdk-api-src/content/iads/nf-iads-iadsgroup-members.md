---
UID: NF:iads.IADsGroup.Members
title: IADsGroup::Members
author: windows-sdk-content
description: Retrieves a collection of the immediate members of the group.
old-location: adsi\iadsgroup_members.htm
old-project: ADSI
ms.assetid: c909f779-ee27-4eb3-aee2-892ccc2a196e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsGroup interface [ADSI],Members method, IADsGroup.Members, IADsGroup::Members, Members, Members method [ADSI], Members method [ADSI],IADsGroup interface, _ds_iadsgroup_members, adsi.iadsgroup__members, adsi.iadsgroup_members, iads/IADsGroup::Members
ms.prod: windows
ms.technology: windows-sdk
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
 - IADsGroup.Members
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim grp As IADsGroup
Dim memberList As IADsMembers
Dim member As IADs

On Error GoTo Cleanup
 
Set grp = GetObject("WinNT://Microsoft/Administrators")
Set memberList = grp.Members
For Each m In memberList
    Set member = m
    Debug.Print member.Name &amp; "(" &amp; member.Class &amp; ")"
Next

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set grp = Nothing
    Set member = Nothing
    Set memberList = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example enumerates all members of a group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumerateGroupMembers(IADsGroup *pGroup)
{
    IADsMembers *pMembers;
    HRESULT hr = S_OK;
    hr = pGroup-&gt;Members(&amp;pMembers);
    if(FAILED(hr)){goto Cleanup;}
 
    hr = EnumMembers(pMembers);  // For more information and a code
                                    example, see IADsMembers::get__NewEnum.
    if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pMembers)
        pMembers-&gt;Release();

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup Property Methods</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>
 

 

