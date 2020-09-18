---
UID: NF:ncryptprotect.NCryptCreateProtectionDescriptor
title: NCryptCreateProtectionDescriptor function (ncryptprotect.h)
description: Retrieves a handle to a protection descriptor object.
helpviewer_keywords: ["NCryptCreateProtectionDescriptor","NCryptCreateProtectionDescriptor function [Security]","ncryptprotect/NCryptCreateProtectionDescriptor","security.ncryptcreateprotectiondescriptor"]
old-location: security\ncryptcreateprotectiondescriptor.htm
tech.root: security
ms.assetid: BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C
ms.date: 12/05/2018
ms.keywords: NCryptCreateProtectionDescriptor, NCryptCreateProtectionDescriptor function [Security], ncryptprotect/NCryptCreateProtectionDescriptor, security.ncryptcreateprotectiondescriptor
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptCreateProtectionDescriptor
 - ncryptprotect/NCryptCreateProtectionDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptCreateProtectionDescriptor
---

# NCryptCreateProtectionDescriptor function


## -description

The <b>NCryptCreateProtectionDescriptor</b> function retrieves a handle to a protection descriptor object.

## -parameters

### -param pwszDescriptorString [in]

Null-terminated Unicode string that contains a protection descriptor rule string or a registered display name for the rule.

If you specify the display name and you want this function to look in the registry for the associated protection descriptor rule string, you must set the <i>dwFlags</i> parameter to <b>NCRYPT_NAMED_DESCRIPTOR_FLAG</b>.

### -param dwFlags [in]

Flag that specifies whether the string in <i>pwszDescriptorString</i> represents the display name of a  protection descriptor and, if so, where in the registry the function should search for the associated protection rule string. The following value combinations can be set:

<ul>
<li>To indicate that the value set in the <i>pwszDescriptorString</i> parameter is a complete protection descriptor rule string rather than a display name, set the <i>dwFlags</i> parameter to zero (0).</li>
<li>To indicate that the string is a display name and that it is saved, along with its associated descriptor rule string, in the <b>HKEY_LOCAL_MACHINE</b> registry hive, bitwise-OR  the <b>NCRYPT_NAMED_DESCRIPTOR_FLAG</b> value and the <b>NCRYPT_MACHINE_KEY_FLAG</b> value.</li>
<li>To indicate that the string is a display name and that it is saved, along with its associated descriptor string rule, in the <b>HKEY_CURRENT_USER</b> registry hive, set only the <b>NCRYPT_NAMED_DESCRIPTOR_FLAG</b> value. That is, there is no unique  flag to specify the current user registry hive.</li>
</ul>
<div class="alert"><b>Note</b>  To associate a descriptor rule with a display name and save both in the registry, call the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname">NCryptRegisterProtectionDescriptorName</a> function.</div>
<div> </div>

### -param phDescriptor [out]

Pointer to a protection descriptor object handle.

## -returns

Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>phDescriptor</i> parameter cannot be <b>NULL</b>.

The <i>pwszDescriptorString</i> parameter cannot be <b>NULL</b> and it cannot be an empty sting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The dwFlags parameter must be <b>NCRYPT_MACHINE_KEY_FLAG</b> or <b>NCRYPT_NAMED_DESCRIPTOR_FLAG</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated to retrieve the registered protection descriptor string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The protection descriptor name specified in the <i>pwszDescriptorString</i> parameter could not be found.

</td>
</tr>
</table>

## -remarks

The protection descriptor object created by this function is an internal data structure that contains information about the descriptor. You cannot use it directly. Your application can, however, use the returned handle in the following functions:

<ul>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor">NCryptCloseProtectionDescriptor</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptgetprotectiondescriptorinfo">NCryptGetProtectionDescriptorInfo</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>
</li>
<li>
<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>
</li>
</ul>
The following examples show protection descriptor rule strings:

<ul>
<li>"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</li>
<li>"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</li>
<li>"LOCAL=user"</li>
<li>"LOCAL=machine"</li>
<li>"WEBCREDENTIALS=MyPasswordName"</li>
<li>"WEBCREDENTIALS=MyPasswordName,myweb.com"</li>
</ul>
You can use the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname">NCryptRegisterProtectionDescriptorName</a> function to associate a display name with a rule string and save both in the registry.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>