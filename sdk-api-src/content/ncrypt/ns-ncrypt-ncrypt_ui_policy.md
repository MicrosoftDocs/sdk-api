---
UID: NS:ncrypt.__NCRYPT_UI_POLICY
title: NCRYPT_UI_POLICY (ncrypt.h)
description: Used with the NCRYPT_UI_POLICY_PROPERTY property to contain strong key user interface information for a key.
helpviewer_keywords: ["NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG","NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG","NCRYPT_UI_POLICY","NCRYPT_UI_POLICY structure [Security]","NCRYPT_UI_PROTECT_KEY_FLAG","ncrypt/NCRYPT_UI_POLICY","security.ncrypt_ui_policy"]
old-location: security\ncrypt_ui_policy.htm
tech.root: security
ms.assetid: 49443042-40bd-4876-8547-e5eb4de503f6
ms.date: 12/05/2018
ms.keywords: NCRYPT_UI_APPCONTAINER_ACCESS_MEDIUM_FLAG, NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG, NCRYPT_UI_POLICY, NCRYPT_UI_POLICY structure [Security], NCRYPT_UI_PROTECT_KEY_FLAG, ncrypt/NCRYPT_UI_POLICY, security.ncrypt_ui_policy
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NCRYPT_UI_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __NCRYPT_UI_POLICY
 - ncrypt/__NCRYPT_UI_POLICY
 - NCRYPT_UI_POLICY
 - ncrypt/NCRYPT_UI_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCRYPT_UI_POLICY
---

# NCRYPT_UI_POLICY structure


## -description

The <b>NCRYPT_UI_POLICY</b> structure is used with the <a href="/windows/desktop/SecCNG/key-storage-property-identifiers">NCRYPT_UI_POLICY_PROPERTY</a> property to contain strong key user interface information for a key. This structure is used with the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsetproperty">NCryptSetProperty</a> and <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptgetproperty">NCryptGetProperty</a> functions with the <a href="/windows/desktop/SecCNG/key-storage-property-identifiers">NCRYPT_UI_POLICY_PROPERTY</a> property.

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