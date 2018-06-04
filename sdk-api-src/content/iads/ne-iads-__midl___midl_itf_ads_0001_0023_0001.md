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

# __MIDL___MIDL_itf_ads_0001_0023_0001 enumeration


## -description


The <b>ADS_GROUP_TYPE_ENUM</b> enumeration specifies the type of group objects in ADSI.


## -enum-fields




### -field ADS_GROUP_TYPE_GLOBAL_GROUP

Specifies a group that can contain accounts from the same domain and other global groups from the same domain. This type of group can be exported to a different domain.


### -field ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP

Specifies a group that can contain accounts from any domain, other domain local groups from the same domain, global groups from any domain, and universal groups. This type of group should not be included in access-control lists of resources in other domains.

This type of group is intended for use with the LDAP provider.


### -field ADS_GROUP_TYPE_LOCAL_GROUP

Specifies a group that is identical to the <b>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</b> group, but is intended for use with the WinNT  provider.


### -field ADS_GROUP_TYPE_UNIVERSAL_GROUP

Specifies a group that can contain accounts from any domain, global groups from any domain,  and other universal groups. This type of group cannot contain domain local groups.


### -field ADS_GROUP_TYPE_SECURITY_ENABLED

Specifies a group that is security enabled. This group can be used to apply an access-control list on an ADSI object or a file system.


## -remarks



Because VBScript cannot read data from a type library, VBScript applications do not understand recognize constants, as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript application. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript application.


#### Examples

The following code example shows how you might use elements of this enumeration.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim rootDSE // IADs
Dim dom // IADsContainer
Dim grp // IADs
Public Const ADS_GROUP_TYPE_GLOBAL_GROUP = &amp;H2
Public Const ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP = &amp;H4
Public Const ADS_GROUP_TYPE_UNIVERSAL_GROUP = &amp;H8
Public Const ADS_GROUP_TYPE_SECURITY_ENABLED = &amp;H80000000

On Error Resume Next
 
Set rootDSE = GetObject("LDAP://RootDSE")
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Exit Sub
End If

Set dom = GetObject("LDAP://" &amp; rootDSE.Get("defaultNamingContext"))
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set rootDSE = Nothing
    Exit Sub
End If

Set rootDSE = Nothing
 
' Creating Secured Global Group.
Set grp = dom.Create("group", "CN=group1")
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set dom = Nothing
    Exit Sub
End If

grp.Put "samAccountName", "group1"
grp.Put "groupType", ADS_GROUP_TYPE_GLOBAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set dom = Nothing
    Set grp = Nothing
    Exit Sub
End If
 
Set grp = Nothing
 
' Creating Distribution List Local Group.
Set grp = dom.Create("group", "CN=group2")
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set dom = Nothing
    Exit Sub
End If

grp.Put "samAccountName", "group2"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP
grp.SetInfo
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set dom = Nothing
    Set grp = Nothing
    Exit Sub
End If

Set grp = Nothing
 
' Create Secured Universal Group (ONLY IN NATIVE MODE).
Set grp = dom.Create("group", "CN=group3")
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
    Set dom = Nothing
    Exit Sub
End If

Set grp = Nothing

grp.Put "samAccountName", "group3"
grp.Put "groupType", ADS_GROUP_TYPE_UNIVERSAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
If (Err.Number&lt;&gt;0) Then
    MsgBox("An error has occurred. " &amp; Err.Number)
End If

Set dom = Nothing
Set grp = Nothing
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>
 

 

