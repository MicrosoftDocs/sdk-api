---
UID: NF:ncryptprotect.NCryptRegisterProtectionDescriptorName
title: NCryptRegisterProtectionDescriptorName function
author: windows-sdk-content
description: Registers the display name and the associated rule string for a protection descriptor.
old-location: security\ncryptregisterprotectiondescriptorname.htm
tech.root: seccng
ms.assetid: DAB03CB2-630F-4BB3-93BD-06BE9126B1C4
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: NCryptRegisterProtectionDescriptorName, NCryptRegisterProtectionDescriptorName function [Security], ncryptprotect/NCryptRegisterProtectionDescriptorName, security.ncryptregisterprotectiondescriptorname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptRegisterProtectionDescriptorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptRegisterProtectionDescriptorName function


## -description


The <b>NCryptRegisterProtectionDescriptorName</b> function registers the display name and the associated rule string for a protection descriptor.


## -parameters




### -param pwszName [in]

Pointer to a null-terminated Unicode string that contains the display name of the descriptor to be registered.


### -param pwszDescriptorString [in, optional]

Pointer to a null-terminated Unicode string that contains a protection descriptor rule. If this parameter is <b>NULL</b> or the string is empty, the registry value previously created for the <i>pwszName</i> parameter will be deleted.


### -param dwFlags

A constant that indicates the registry hive under which to register the new entry. If this value is zero (0), the registry root is <b>HKEY_CURRENT_USER</b>. If this value is <b>NCRYPT_MACHINE_KEY_FLAG</b>, the root is <b>HKEY_LOCAL_MACHINE</b>.


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



The registry key created by using this function is not volatile. The information is stored in a file and preserved when the computer shuts down.




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/32953AEC-01EE-4ED1-80F3-29963F43004F">NCryptQueryProtectionDescriptorName</a>
 

 

