---
UID: NF:iads.IADsGroup.Add
title: IADsGroup::Add
author: windows-sdk-content
description: Adds an ADSI object to an existing group.
old-location: adsi\iadsgroup_add.htm
old-project: ADSI
ms.assetid: 7b660c3b-f395-407e-bc84-7ef7117298bb
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Add, Add method [ADSI], Add method [ADSI],IADsGroup interface, IADsGroup interface [ADSI],Add method, IADsGroup.Add, IADsGroup::Add, _ds_iadsgroup_add, adsi.iadsgroup__add, adsi.iadsgroup_add, iads/IADsGroup::Add
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
 - IADsGroup.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsGroup::Add


## -description


The <b>IADsGroup::Add</b> method adds an ADSI object to an existing group.


## -parameters




### -param bstrNewItem [in]

Contains a <b>BSTR</b> that specifies the ADsPath of the object to add to the group. For more information, see Remarks.


## -returns



The following are the most common return values. For more information about return values, see <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



If the LDAP provider is used to bind to the <a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a> object, the same form of ADsPath must be specified in the <i>bstrNewItem</i> parameter. For example, if the ADsPath used to bind to the <b>IADsGroup</b> object includes a server, the ADsPath in the <i>bstrNewItem</i> parameter must contain the same server prefix. Likewise, if a serverless path is used to bind to the <b>IADsGroup</b> object, the <i>bstrNewItem</i> parameter must also contain a serverless path. When using server prefix, delays may occur if the group and the new member are from different domains, as requests may be sent to the wrong domain controller and referred to a domain controller of the correct domain and retried there. An exception occurs when adding or removing a member using a GUID or security identifier (SID) ADsPath. In this case, a serverless path should always be used in <i>bstrNewItem</i>.

The LDAP provider for Active Directory enables a member to be added to a group using the string form of the member SID. The <i>bstrNewItem</i> parameter can contain a SID string in the following form.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LDAP://SID=&lt;010500000000000515000000c6bb507afbda8b7f43170a325b040000&gt;</pre>
</td>
</tr>
</table></span></div>
For more information about SID strings in Active Directory, see <a href="https://msdn.microsoft.com/18b4613c-eb93-4204-96f2-0f91d7900587">Binding to an Object Using a SID</a>.

The WinNT provider for Active Directory also enables a member to be added to a group using the string form of the member's SID. The <i>bstrNewItem</i> parameter can contain a SID string in the following form.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WinNT://S-1-5-21-35135249072896"</pre>
</td>
</tr>
</table></span></div>

#### Examples

The following code example shows how to add a user object ("jeff") to the group ("Administrators") on the "Fabrikam" domain, using the WinNT provider.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim grp As IADsGroup
Set grp = GetObject("WinNT://Fabrikam/Administrators")
grp.Add ("WinNT://Fabrikam/jeff")</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to add a user object to a group using the LDAP provider.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("LDAP://CN=Administrators, CN=Users, DC=Fabrikam, DC=com")
grp.Add("LDAP://CN=Jeff Smith, OU=Sales,DC=Fabrikam,DC=com")

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set grp = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example adds an existing user account to the Administrators group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://Fabrikam/Administrators";
hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&amp;pGroup);
if(FAILED(hr)) {goto Cleanup;}

// This assumes that the "WinNT://Fabrikam/jeff" user account exists 
// and does not already belong to the Administrators group.

hr = pGroup-&gt;Add(_bstr_t("WinNT://Fabrikam/jeff"));
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup)
        pGroup-&gt;Release();

    return hr;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/18b4613c-eb93-4204-96f2-0f91d7900587">Binding to an Object Using a SID</a>



<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup Property Methods</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>
 

 

