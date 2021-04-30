---
UID: NF:iads.IADsSecurityUtility.SetSecurityDescriptor
title: IADsSecurityUtility::SetSecurityDescriptor (iads.h)
description: Sets the security descriptor for the specified file, file share, or registry key.
helpviewer_keywords: ["File","File share","IADsSecurityUtility interface [ADSI]","SetSecurityDescriptor method","IADsSecurityUtility.SetSecurityDescriptor","IADsSecurityUtility::SetSecurityDescriptor","Registry key","SetSecurityDescriptor","SetSecurityDescriptor method [ADSI]","SetSecurityDescriptor method [ADSI]","IADsSecurityUtility interface","_ds_iadssecurityutility_setsecuritydescriptor","adsi.iadssecurityutility__setsecuritydescriptor","adsi.iadssecurityutility_setsecuritydescriptor","iads/IADsSecurityUtility::SetSecurityDescriptor"]
old-location: adsi\iadssecurityutility_setsecuritydescriptor.htm
tech.root: adsi
ms.assetid: f0f5c1fb-14fa-4d84-aa82-0d5e24ec5c2b
ms.date: 12/05/2018
ms.keywords: File, File share, IADsSecurityUtility interface [ADSI],SetSecurityDescriptor method, IADsSecurityUtility.SetSecurityDescriptor, IADsSecurityUtility::SetSecurityDescriptor, Registry key, SetSecurityDescriptor, SetSecurityDescriptor method [ADSI], SetSecurityDescriptor method [ADSI],IADsSecurityUtility interface, _ds_iadssecurityutility_setsecuritydescriptor, adsi.iadssecurityutility__setsecuritydescriptor, adsi.iadssecurityutility_setsecuritydescriptor, iads/IADsSecurityUtility::SetSecurityDescriptor
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
 - IADsSecurityUtility::SetSecurityDescriptor
 - iads/IADsSecurityUtility::SetSecurityDescriptor
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
 - IADsSecurityUtility.SetSecurityDescriptor
---

# IADsSecurityUtility::SetSecurityDescriptor


## -description

The <b>SetSecurityDescriptor</b> method sets the security descriptor for the specified file, file share, or registry key.

## -parameters

### -param varPath [in]

A <b>VARIANT</b> string that contains the path of the object to set the security descriptor for. Possible values are listed in the following list.



#### File

A valid file path syntax. For example: "c:\specs\public\adxml.doc" or "\\adsi\public\dsclient.exe".



#### File share

A valid file path syntax for a file share. For example: "\\adsi\public".



#### Registry key

A valid registry syntax. For example, "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ADs".

### -param lPathFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a> values which specifies the format of the <i>varPath</i> parameter.

### -param varData [in]

A <b>VARIANT</b> that contains the new security descriptor. The format of the security descriptor is specified by the <i>lDataFormat</i> parameter.

### -param lDataFormat [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor contained in the <i>VarData</i> parameter. The following list identifies the possible values for this parameter and the format of the <i>VarData</i> parameter.

## -returns

Returns <b>S_OK</b> if successful or a COM or Win32 error code otherwise. Possible error codes are listed in the following list.

## -remarks

Access control entries must appear in the following order in a security descriptor's access control list:

<ul>
<li>Access-denied ACEs that apply to the object itself</li>
<li>Access-denied ACEs that apply to a child of the object, such as a property set or property</li>
<li>Access-allowed ACEs that apply to the object itself</li>
<li>Access-allowed ACEs that apply to a child of the object, such as a property set or property</li>
<li>All inherited ACEs</li>
</ul>



#### Examples

The following code example shows how to set a security descriptor for a file.


```vb
Dim dacl as IADsAccessControlList
Dim sd as IADsSecurityDescriptor
Dim newAce as New AccessControlEntry
Dim sdUtil as New ADsSecurityUtility

Set sd = sdUtil.GetSecurityDescriptor("c:\specs\adsixml.doc", ADS_PATH_FILE, ADS_SD_FORMAT_IID )
Set dacl = sd.DiscretionaryAcl
 
' Add a new ACE for Jeff Smith. 
newAce.Trustee = "Fabrikam\jeffsmith" 
newAce.AccessMask = ADS_RIGHT_GENERIC_READ Or ADS_RIGHT_GENERIC_EXECUTE 

newAce.AceType = ADS_ACETYPE_ACCESS_ALLOWED 

dacl.AddAce newAce 
sd.DiscretionaryAcl = dacl 
sdUtil.SetSecurityDescriptor "c:\specs\adsixml.doc", ADS_PATH_FILE, sd, ADS_SD_FORMAT_IID

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dacl = Nothing
    Set sd = Nothing
    Set newAce = Nothing
    Set sdUtil = Nothing

```

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-convertsecuritydescriptor">ConvertSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>