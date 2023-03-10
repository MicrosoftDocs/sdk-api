---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0023_0001
title: ADS_GROUP_TYPE_ENUM (iads.h)
description: Specifies the type of group objects in ADSI.
helpviewer_keywords: ["ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP","ADS_GROUP_TYPE_ENUM","ADS_GROUP_TYPE_ENUM enumeration [ADSI]","ADS_GROUP_TYPE_GLOBAL_GROUP","ADS_GROUP_TYPE_LOCAL_GROUP","ADS_GROUP_TYPE_SECURITY_ENABLED","ADS_GROUP_TYPE_UNIVERSAL_GROUP","_ds_ads_group_type_enum","adsi.ads__group__type__enum","adsi.ads_group_type_enum","iads/ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP","iads/ADS_GROUP_TYPE_ENUM","iads/ADS_GROUP_TYPE_GLOBAL_GROUP","iads/ADS_GROUP_TYPE_LOCAL_GROUP","iads/ADS_GROUP_TYPE_SECURITY_ENABLED","iads/ADS_GROUP_TYPE_UNIVERSAL_GROUP"]
old-location: adsi\ads_group_type_enum.htm
tech.root: adsi
ms.assetid: c046ffbf-15e2-44d7-a997-f992c6289bcd
ms.date: 12/05/2018
ms.keywords: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP, ADS_GROUP_TYPE_ENUM, ADS_GROUP_TYPE_ENUM enumeration [ADSI], ADS_GROUP_TYPE_GLOBAL_GROUP, ADS_GROUP_TYPE_LOCAL_GROUP, ADS_GROUP_TYPE_SECURITY_ENABLED, ADS_GROUP_TYPE_UNIVERSAL_GROUP, _ds_ads_group_type_enum, adsi.ads__group__type__enum, adsi.ads_group_type_enum, iads/ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP, iads/ADS_GROUP_TYPE_ENUM, iads/ADS_GROUP_TYPE_GLOBAL_GROUP, iads/ADS_GROUP_TYPE_LOCAL_GROUP, iads/ADS_GROUP_TYPE_SECURITY_ENABLED, iads/ADS_GROUP_TYPE_UNIVERSAL_GROUP
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADS_GROUP_TYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0023_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0023_0001
 - ADS_GROUP_TYPE_ENUM
 - iads/ADS_GROUP_TYPE_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_GROUP_TYPE_ENUM
---

# ADS_GROUP_TYPE_ENUM enumeration


## -description

The <b>ADS_GROUP_TYPE_ENUM</b> enumeration specifies the type of group objects in ADSI.

## -enum-fields

### -field ADS_GROUP_TYPE_GLOBAL_GROUP:0x2

Specifies a group that can contain accounts from the same domain and other global groups from the same domain. This type of group can be exported to a different domain.

### -field ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP:0x4

Specifies a group that can contain accounts from any domain, other domain local groups from the same domain, global groups from any domain, and universal groups. This type of group should not be included in access-control lists of resources in other domains.

This type of group is intended for use with the LDAP provider.

### -field ADS_GROUP_TYPE_LOCAL_GROUP:0x4

Specifies a group that is identical to the <b>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</b> group, but is intended for use with the WinNT  provider.

### -field ADS_GROUP_TYPE_UNIVERSAL_GROUP:0x8

Specifies a group that can contain accounts from any domain, global groups from any domain,  and other universal groups. This type of group cannot contain domain local groups.

### -field ADS_GROUP_TYPE_SECURITY_ENABLED:0x80000000

Specifies a group that is security enabled. This group can be used to apply an access-control list on an ADSI object or a file system.

## -remarks

Because VBScript cannot read data from a type library, VBScript applications do not understand recognize constants, as defined above. Use the numerical constants, instead, to set the appropriate flags in your VBScript application. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript application.


#### Examples

The following code example shows how you might use elements of this enumeration.


```vb
Dim rootDSE // IADs
Dim dom // IADsContainer
Dim grp // IADs
Public Const ADS_GROUP_TYPE_GLOBAL_GROUP = &H2
Public Const ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP = &H4
Public Const ADS_GROUP_TYPE_UNIVERSAL_GROUP = &H8
Public Const ADS_GROUP_TYPE_SECURITY_ENABLED = &H80000000

On Error Resume Next
 
Set rootDSE = GetObject("LDAP://RootDSE")
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Exit Sub
End If

Set dom = GetObject("LDAP://" & rootDSE.Get("defaultNamingContext"))
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set rootDSE = Nothing
    Exit Sub
End If

Set rootDSE = Nothing
 
' Creating Secured Global Group.
Set grp = dom.Create("group", "CN=group1")
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set dom = Nothing
    Exit Sub
End If

grp.Put "samAccountName", "group1"
grp.Put "groupType", ADS_GROUP_TYPE_GLOBAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set dom = Nothing
    Set grp = Nothing
    Exit Sub
End If
 
Set grp = Nothing
 
' Creating Distribution List Local Group.
Set grp = dom.Create("group", "CN=group2")
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set dom = Nothing
    Exit Sub
End If

grp.Put "samAccountName", "group2"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP
grp.SetInfo
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set dom = Nothing
    Set grp = Nothing
    Exit Sub
End If

Set grp = Nothing
 
' Create Secured Universal Group (ONLY IN NATIVE MODE).
Set grp = dom.Create("group", "CN=group3")
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
    Set dom = Nothing
    Exit Sub
End If

Set grp = Nothing

grp.Put "samAccountName", "group3"
grp.Put "groupType", ADS_GROUP_TYPE_UNIVERSAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
If (Err.Number<>0) Then
    MsgBox("An error has occurred. " & Err.Number)
End If

Set dom = Nothing
Set grp = Nothing

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI
  Enumerations</a>
