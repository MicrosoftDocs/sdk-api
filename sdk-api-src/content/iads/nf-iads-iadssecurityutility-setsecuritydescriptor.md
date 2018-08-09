---
UID: NF:iads.IADsSecurityUtility.SetSecurityDescriptor
title: IADsSecurityUtility::SetSecurityDescriptor
author: windows-sdk-content
description: Sets the security descriptor for the specified file, file share, or registry key.
old-location: adsi\iadssecurityutility_setsecuritydescriptor.htm
old-project: ADSI
ms.assetid: f0f5c1fb-14fa-4d84-aa82-0d5e24ec5c2b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: File, File share, IADsSecurityUtility interface [ADSI],SetSecurityDescriptor method, IADsSecurityUtility.SetSecurityDescriptor, IADsSecurityUtility::SetSecurityDescriptor, Registry key, SetSecurityDescriptor, SetSecurityDescriptor method [ADSI], SetSecurityDescriptor method [ADSI],IADsSecurityUtility interface, _ds_iadssecurityutility_setsecuritydescriptor, adsi.iadssecurityutility__setsecuritydescriptor, adsi.iadssecurityutility_setsecuritydescriptor, iads/IADsSecurityUtility::SetSecurityDescriptor
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
 - IADsSecurityUtility.SetSecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
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

Contains one of the <a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a> values which specifies the format of the <i>varPath</i> parameter.


### -param varData




### -param lDataFormat [in]

Contains one of the <a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a> values which specifies the format of the security descriptor contained in the <i>VarData</i> parameter. The following list identifies the possible values for this parameter and the format of the <i>VarData</i> parameter.


#### - VarData [in]

A <b>VARIANT</b> that contains the new security descriptor. The format of the security descriptor is specified by the <i>lDataFormat</i> parameter.


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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim dacl as IADsAccessControlList
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
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set dacl = Nothing
    Set sd = Nothing
    Set newAce = Nothing
    Set sdUtil = Nothing
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3ae0ec98-9184-4ab3-b859-39c0d677eb0d">ADS_PATHTYPE_ENUM</a>



<a href="https://msdn.microsoft.com/503247b6-3119-4514-9831-c8f0ef50c0fa">ADS_SD_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/ea6509bd-5625-458b-be7a-abb43ba2f46e">ConvertSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>
 

 

