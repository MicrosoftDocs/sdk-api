---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IADsGroup::Remove


## -description


The <b>IADsGroup::Remove</b> method removes the specified user object from this group. The operation does not remove the group object itself even when there is no member remaining in the group.


## -parameters




### -param bstrItemToBeRemoved [in]

Contains a <b>BSTR</b> that specifies the ADsPath of the object to remove from the group. For more information about this parameter, see the Remarks section.


## -returns



The following are the most common return values. For more information about return values, see <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



If the LDAP provider is used to bind to the <a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a> object, the same form of ADsPath must be specified in the <i>bstrItemToBeRemoved</i> parameter. For example, if the ADsPath used to bind to the <b>IADsGroup</b> object includes a server, the ADsPath in the <i>bstrItemToBeRemoved</i> parameter must contain the same server prefix. Likewise, if a serverless path is used to bind to the <b>IADsGroup</b> object, the <i>bstrItemToBeRemoved</i> parameter must also contain a serverless path. The exception is when adding or removing a member using a GUID or SID ADsPath. In this case, a serverless path should always be used in <i>bstrItemToBeRemoved</i>.

You can use a SID in the ADsPath to remove a security principal from the group through the WinNT provider. For example, suppose the SID of a user, "Fabrikam\jeffsmith", is S-1-5-21-35135249072896, the following statement:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim group As IADsGroup
group.Remove("WinNT://S-1-5-21-35135249072896")</pre>
</td>
</tr>
</table></span></div>
is equivalent to

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim group As IADsGroup
group.Remove("WinNT://Fabrikam/jeffsmith")</pre>
</td>
</tr>
</table></span></div>
Removing a member using its SID through the WinNT provider is a new feature in Windows 2000 and the DSCLIENT package.


#### Examples

The following code example removes a user account from a group.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Fabrikam/Administrators")
grp.Remove ("WinNT://Fabrikam/jeffsmith")

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set grp = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example removes a user from a group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR usrPath = L"WinNT://Fabrikam/jeffsmith";
LPWSTR grpPath = L"WinNT://Fabrikam/Administrators";

hr = ADsGetObject(grpPath, IID_IADsGroup, (void**)&amp;pGroup);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup-&gt;Remove(CComBSTR(usrPath));
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup)
        pGroup-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/dbf0c424-e906-4a72-a369-81bf96275bbc">IADsGroup</a>



<a href="https://msdn.microsoft.com/a8aa88d4-4695-47bc-bf7f-a17236a5671c">IADsGroup Property Methods</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>
 

 

