---
UID: NS:ncrypt.__NCRYPT_UI_POLICY
title: "__NCRYPT_UI_POLICY"
author: windows-sdk-content
description: Used with the NCRYPT_UI_POLICY_PROPERTY property to contain strong key user interface information for a key.
old-location: security\ncrypt_ui_policy.htm
old-project: SecCNG
ms.assetid: 49443042-40bd-4876-8547-e5eb4de503f6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG, NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG, NCRYPT_UI_POLICY, NCRYPT_UI_POLICY structure [Security], NCRYPT_UI_PROTECT_KEY_FLAG, __NCRYPT_UI_POLICY, ncrypt/NCRYPT_UI_POLICY, security.ncrypt_ui_policy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NCRYPT_UI_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCRYPT_UI_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __NCRYPT_UI_POLICY structure


## -description


The <b>NCRYPT_UI_POLICY</b> structure is used with the <a href="https://msdn.microsoft.com/407f0e42-07c8-4ec6-81c6-f8bde005adb0">NCRYPT_UI_POLICY_PROPERTY</a> property to contain strong key user interface information for a key. This structure is used with the <a href="https://msdn.microsoft.com/ad1148aa-5f64-4867-9e17-6b41cc0c20b7">NCryptSetProperty</a> and <a href="https://msdn.microsoft.com/7b857ce0-8525-489b-9987-ef40081a5577">NCryptGetProperty</a> functions with the <a href="https://msdn.microsoft.com/407f0e42-07c8-4ec6-81c6-f8bde005adb0">NCRYPT_UI_POLICY_PROPERTY</a> property.


## -struct-fields




### -field dwVersion

The version number of the structure. This member must contain 1.


### -field dwFlags

A set of flags that provide additional user interface information or requirements.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_UI_PROTECT_KEY_FLAG"></a><a id="ncrypt_ui_protect_key_flag"></a><dl>
<dt><b>NCRYPT_UI_PROTECT_KEY_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Display the strong key user interface as needed.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></a><a id="ncrypt_ui_force_high_protection_flag"></a><dl>
<dt><b>NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Force high protection.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG"></a><a id="ncrypt_ui_appcontainer_access_medium_flag"></a><dl>
<dt><b>NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
An app container has accessed a medium key that is not strongly protected. For example, a key that is for user consent only, or is password or fingerprint protected.

</td>
</tr>
</table>
 


### -field pszCreationTitle

A pointer to a null-terminated Unicode string that contains the text that will be used in the title of the strong key dialog box when the key is completed. If this member is <b>NULL</b>, a default creation title will be used in the strong key dialog box.  This member is only used on key finalization.


### -field pszFriendlyName

A pointer to a null-terminated Unicode string that contains the text that will be displayed in the strong key dialog box as the name of the key. If this member is <b>NULL</b>, a default name will be used in the strong key dialog box.  This member is used both when the key is completed and when the key is used.


### -field pszDescription

A pointer to a null-terminated Unicode string that contains the text that will be displayed in the strong key dialog box as the description of the key. If this member is <b>NULL</b>, a default description will be used in the strong key dialog box.  This member is used both when the key is completed and when the key is used.

