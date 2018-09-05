---
UID: NF:ncrypt.NCryptGetProperty
title: NCryptGetProperty function
author: windows-sdk-content
description: Retrieves the value of a named property for a key storage object.
old-location: security\ncryptgetproperty_func.htm
old-project: SecCNG
ms.assetid: 7b857ce0-8525-489b-9987-ef40081a5577
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, NCRYPT_PERSIST_ONLY_FLAG, NCRYPT_SILENT_FLAG, NCryptGetProperty, NCryptGetProperty function [Security], OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, ncrypt/NCryptGetProperty, security.ncryptgetproperty_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: SESSION_HEADER, *PSESSION_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptGetProperty
product: Windows
targetos: Windows
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NCryptGetProperty function


## -description


The <b>NCryptGetProperty</b> function retrieves the value of a named property for a key storage object.


## -parameters




### -param hObject [in]

The handle of the object to get the property for. This can be a provider handle (<b>NCRYPT_PROV_HANDLE</b>) or a key handle (<b>NCRYPT_KEY_HANDLE</b>).


### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to retrieve. This can be one of the predefined <a href="https://msdn.microsoft.com/407f0e42-07c8-4ec6-81c6-f8bde005adb0">Key Storage Property Identifiers</a> or a custom property identifier.


### -param pbOutput [out]

The address of a buffer that receives the property value. The <i>cbOutput</i> parameter contains the size of this buffer.

 To calculate the size required for the buffer, set this parameter to <b>NULL</b>. The size, in bytes, required is returned in the location pointed to by the <i>pcbResult</i> parameter.


### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer.


### -param pcbResult [out]

A pointer to a <b>DWORD</b> variable that receives the number of bytes that were copied to the <i>pbOutput</i> buffer.

If the <i>pbOutput</i> parameter is <b>NULL</b>, the size, in bytes, required for the buffer is placed in the location pointed to by this parameter.


### -param dwFlags [in]

Flags that modify function behavior. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PERSIST_ONLY_FLAG"></a><a id="ncrypt_persist_only_flag"></a><dl>
<dt><b>NCRYPT_PERSIST_ONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Ignore any built in values for this property and only retrieve the user-persisted properties of the key.  The maximum size of the data for any persisted property is <b>NCRYPT_MAX_PROPERTY_DATA</b> bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


For the <b>NCRYPT_SECURITY_DESCR_PROPERTY</b> property, this parameter must also contain one of the following values, which identifies the part of the security descriptor to retrieve.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OWNER_SECURITY_INFORMATION"></a><a id="owner_security_information"></a><dl>
<dt><b>OWNER_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the security identifier (SID) of the object's owner. Use the <a href="https://msdn.microsoft.com/58e810db-348e-430c-a61f-79f67826b60d">GetSecurityDescriptorOwner</a> function to obtain the owner SID from the <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the SID of the object's primary group. Use the <a href="https://msdn.microsoft.com/a920b49e-a4c2-4e49-b529-88c12205d995">GetSecurityDescriptorGroup</a> function to obtain the group SID from the <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the discretionary access control list (DACL). Use the <a href="https://msdn.microsoft.com/6bf59735-aaa3-4751-8c98-00cc197df4e5">GetSecurityDescriptorSacl</a> function to obtain the DACL from the <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the system access control list (SACL). Use the <a href="https://msdn.microsoft.com/8006c8bb-4976-463f-b074-a59c3bbab36b">GetSecurityDescriptorDacl</a> function to obtain the SACL from the <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
</table>
 


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



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
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hObject</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The specified property is not supported for the object.

</td>
</tr>
</table>
 




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



