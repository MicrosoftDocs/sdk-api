---
UID: NF:ncryptprotect.NCryptQueryProtectionDescriptorName
title: NCryptQueryProtectionDescriptorName function (ncryptprotect.h)
description: Retrieves the protection descriptor rule string associated with a registered descriptor display name.
helpviewer_keywords: ["NCryptQueryProtectionDescriptorName","NCryptQueryProtectionDescriptorName function [Security]","ncryptprotect/NCryptQueryProtectionDescriptorName","security.ncryptqueryprotectiondescriptorname"]
old-location: security\ncryptqueryprotectiondescriptorname.htm
tech.root: security
ms.assetid: 32953AEC-01EE-4ED1-80F3-29963F43004F
ms.date: 12/05/2018
ms.keywords: NCryptQueryProtectionDescriptorName, NCryptQueryProtectionDescriptorName function [Security], ncryptprotect/NCryptQueryProtectionDescriptorName, security.ncryptqueryprotectiondescriptorname
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
 - NCryptQueryProtectionDescriptorName
 - ncryptprotect/NCryptQueryProtectionDescriptorName
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
 - NCryptQueryProtectionDescriptorName
---

# NCryptQueryProtectionDescriptorName function


## -description

The <b>NCryptQueryProtectionDescriptorName</b> function retrieves the protection descriptor rule string associated with a registered descriptor display name.

## -parameters

### -param pwszName [in]

The registered display name for the protection descriptor. Register a name by calling the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname">NCryptRegisterProtectionDescriptorName</a> function.

### -param pwszDescriptorString [out]

A null-terminated Unicode string that contains the protection descriptor rule. Set this value to <b>NULL</b> and set the size of the descriptor string pointed to by <i>pcDescriptorString</i> argument to zero on your initial call to this function. For more information, see Remarks.

### -param pcDescriptorString [in, out]

Pointer to a variable that contains the number  of characters in the string retrieved in the <i>pwszDescriptorString</i> parameter. Set the variable to zero on your initial call to this function. For more information, see Remarks.

### -param dwFlags

Flag that specifies which registry hive to query for the registered name. This can be zero to look in the <b>HKEY_CURRENT_USER</b> hive or you can specify <b>NCRYPT_MACHINE_KEY_FLAG</b> to query the <b>HKEY_LOCAL_MACHINE</b> hive.

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
The <i>pwszName</i> parameter cannot be <b>NULL</b>, and the value pointed to by the parameter cannot be an empty string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter must be zero or <b>NCRYPT_MACHINE_KEY_FLAG</b>.

</td>
</tr>
</table>

## -remarks

To retrieve a protection descriptor rule string, you must call this function twice. The first time you call, set the <i>pwszDescriptorString</i> argument to <b>NULL</b> and the value pointed to by the <i>pcDescriptorString</i> argument to zero. Your first call retrieves the number of characters in the descriptor string. Use this number to allocate memory for the string and retrieve a pointer to the allocated buffer. To retrieve the string, call the function again using the pointer.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname">NCryptRegisterProtectionDescriptorName</a>