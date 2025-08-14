---
UID: NF:ncrypt.NCryptSetProperty
title: NCryptSetProperty function (ncrypt.h)
description: Sets the value for a named property for a CNG key storage object.
helpviewer_keywords: ["DACL_SECURITY_INFORMATION","GROUP_SECURITY_INFORMATION","LABEL_SECURITY_INFORMATION","NCRYPT_PERSIST_FLAG","NCRYPT_PERSIST_ONLY_FLAG","NCRYPT_SILENT_FLAG","NCryptSetProperty","NCryptSetProperty function [Security]","OWNER_SECURITY_INFORMATION","SACL_SECURITY_INFORMATION","ncrypt/NCryptSetProperty","security.ncryptsetproperty_func"]
old-location: security\ncryptsetproperty_func.htm
tech.root: security
ms.assetid: ad1148aa-5f64-4867-9e17-6b41cc0c20b7
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, LABEL_SECURITY_INFORMATION, NCRYPT_PERSIST_FLAG, NCRYPT_PERSIST_ONLY_FLAG, NCRYPT_SILENT_FLAG, NCryptSetProperty, NCryptSetProperty function [Security], OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, ncrypt/NCryptSetProperty, security.ncryptsetproperty_func
req.header: ncrypt.h
req.include-header: 
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptSetProperty
 - ncrypt/NCryptSetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptSetProperty
---

# NCryptSetProperty function


## -description

The <b>NCryptSetProperty</b> function sets the value for a named property for a CNG key storage object.

## -parameters

### -param hObject [in]

The handle of the key storage object to set the property for.

### -param pszProperty [in]

A pointer to a null-terminated Unicode string that contains the name of the property to set. This can be one of the predefined <a href="/windows/desktop/SecCNG/key-storage-property-identifiers">Key Storage Property Identifiers</a> or a custom property identifier.

### -param pbInput [in]

The address of a buffer that contains the new property value. The <i>cbInput</i> parameter contains the size of this buffer.

### -param cbInput [in]

The size, in bytes, of the <i>pbInput</i> buffer.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PERSIST_FLAG"></a><a id="ncrypt_persist_flag"></a><dl>
<dt><b>NCRYPT_PERSIST_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The property should be stored in key storage along with the key material. This flag can only be used when the <i>hObject</i> parameter is the handle of a persisted key. The maximum size of the data for any persisted property is <b>NCRYPT_MAX_PROPERTY_DATA</b> bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PERSIST_ONLY_FLAG"></a><a id="ncrypt_persist_only_flag"></a><dl>
<dt><b>NCRYPT_PERSIST_ONLY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Do not overwrite any built-in values for this property and only set the user-persisted properties of the key.  The maximum size of the data for any persisted property is <b>NCRYPT_MAX_PROPERTY_DATA</b> bytes. This flag cannot be used with the <b>NCRYPT_SECURITY_DESCR_PROPERTY</b> property.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>
 


For the <b>NCRYPT_SECURITY_DESCR_PROPERTY</b> property, this parameter must also contain one of the following values, which identifies the part of the security descriptor to set.



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
Set the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the object's owner. Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner">SetSecurityDescriptorOwner</a> function to set the owner SID in the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="GROUP_SECURITY_INFORMATION"></a><a id="group_security_information"></a><dl>
<dt><b>GROUP_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Set the SID of the object's primary group. Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup">SetSecurityDescriptorGroup</a> function to set the group SID in the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="DACL_SECURITY_INFORMATION"></a><a id="dacl_security_information"></a><dl>
<dt><b>DACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Set the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL). Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a> function to set the DACL in the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SACL_SECURITY_INFORMATION"></a><a id="sacl_security_information"></a><dl>
<dt><b>SACL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Set the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a> function to set the SACL in the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="LABEL_SECURITY_INFORMATION"></a><a id="label_security_information"></a><dl>
<dt><b>LABEL_SECURITY_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Set the mandatory label access control entry in the SACL of the object. Use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a> function to set the SACL in the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure. For more information about the mandatory label access control entry, see <a href="/previous-versions/dotnet/articles/bb625963(v=msdn.10)">Windows Integrity Mechanism Design</a>.

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

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.
