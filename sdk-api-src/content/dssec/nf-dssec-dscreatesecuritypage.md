---
UID: NF:dssec.DSCreateSecurityPage
title: DSCreateSecurityPage function
author: windows-sdk-content
description: Creates a security property page for an Active Directory object.
old-location: security\dscreatesecuritypage.htm
tech.root: secauthz
ms.assetid: 1ebb531f-84a0-4ace-88d1-89e65e18c34a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: DSCreateSecurityPage, DSCreateSecurityPage function [Security], DSSI_IS_ROOT, DSSI_NO_ACCESS_CHECK, DSSI_NO_EDIT_OWNER, DSSI_NO_EDIT_SACL, DSSI_NO_FILTER, DSSI_NO_READONLY_MESSAGE, DSSI_READ_ONLY, dssec/DSCreateSecurityPage, security.dscreatesecuritypage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dssec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DSSec.lib
req.dll: DSSec.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DSSec.dll
api_name:
 - DSCreateSecurityPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSCreateSecurityPage function


## -description


The <b>DSCreateSecurityPage</b> function creates a security property page for an Active Directory object. The resulting property page can be added to a property sheet.


## -parameters




### -param pwszObjectPath [in]

A pointer to a <b>null</b>-terminated wide character string that represents the full Active Directory path for the object.


### -param pwszObjectClass [in, optional]

A pointer to a <b>null</b>-terminated wide character string that represents the object class. This value can be <b>NULL</b>. 


### -param dwFlags [in]

Flags used for the security property page. This parameter can be none or any combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DSSI_READ_ONLY"></a><a id="dssi_read_only"></a><dl>
<dt><b>DSSI_READ_ONLY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The security properties are read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_ACCESS_CHECK_"></a><a id="dssi_no_access_check_"></a><dl>
<dt><b>DSSI_NO_ACCESS_CHECK </b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
No access check is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_EDIT_SACL"></a><a id="dssi_no_edit_sacl"></a><dl>
<dt><b>DSSI_NO_EDIT_SACL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) property is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_EDIT_OWNER"></a><a id="dssi_no_edit_owner"></a><dl>
<dt><b>DSSI_NO_EDIT_OWNER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The object owner property is read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_IS_ROOT"></a><a id="dssi_is_root"></a><dl>
<dt><b>DSSI_IS_ROOT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
The object is a root object.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_FILTER"></a><a id="dssi_no_filter"></a><dl>
<dt><b>DSSI_NO_FILTER</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Do not apply any filters.

</td>
</tr>
<tr>
<td width="40%"><a id="DSSI_NO_READONLY_MESSAGE"></a><a id="dssi_no_readonly_message"></a><dl>
<dt><b>DSSI_NO_READONLY_MESSAGE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Suppress read-only popup messages.

</td>
</tr>
</table>
 


### -param phPage [out]

A pointer to a <b>HPROPSHEETPAGE</b> that returns the created security property page.


### -param pfnReadSD [in, optional]

A pointer to a function used to read the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> of the object. This value can be <b>NULL</b>. If <i>pfnReadSD</i> is not <b>NULL</b>, <b>DSCreateSecurityPage</b>  calls the function referenced by <i>pfnReadSD</i> to retrieve the security descriptor of the object.


### -param pfnWriteSD [in, optional]

A pointer to  a function used to write the security descriptor of the object. This value can be <b>NULL</b>. If <i>pfnWriteSD</i> is not <b>NULL</b>, <b>DSCreateSecurityPage</b>  calls the function referenced by <i>pfnWriteSD</i> to write the security descriptor of the object.


### -param lpContext [in]

Context to pass to the functions identified by <i>pfnReadSD</i> or <i>pfnWriteSD</i>.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The function pointed to by <i>pfnReadSD</i> is defined as follows.


```cpp
#include <windows.h>

typedef HRESULT (WINAPI *PFNREADOBJECTSECURITY)(
    LPCWSTR,               // Active Directory path of object
    SECURITY_INFORMATION,  // the security information to read
    PSECURITY_DESCRIPTOR*, // the returned security descriptor 
    LPARAM                 // context parameter
);

```


The <b>DSCreateSecurityPage</b> function will free the security descriptor returned in the third parameter above by a  call to the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.

The function pointed to by <i>pfnWriteSD</i> is defined as follows.


```cpp
#include <windows.h>

typedef HRESULT (WINAPI *PFNWRITEOBJECTSECURITY)(
    LPCWSTR,              // Active Directory path of object
    SECURITY_INFORMATION, // the security information to write
    PSECURITY_DESCRIPTOR, // the security descriptor to write
    LPARAM                // context parameter
);

```





## -see-also




<a href="https://msdn.microsoft.com/6623fe7e-e91d-49c7-9ad0-7791c178d12b">Basic Security Property Page</a>



<a href="https://msdn.microsoft.com/38d94f36-f149-4b62-a710-8f7359bfd8cd">ISecurityInformation</a>
 

 

