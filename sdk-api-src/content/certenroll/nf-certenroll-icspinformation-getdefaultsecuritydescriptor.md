---
UID: NF:certenroll.ICspInformation.GetDefaultSecurityDescriptor
title: ICspInformation::GetDefaultSecurityDescriptor (certenroll.h)
description: Retrieves the default private key security descriptor.
helpviewer_keywords: ["GetDefaultSecurityDescriptor","GetDefaultSecurityDescriptor method [Security]","GetDefaultSecurityDescriptor method [Security]","ICspInformation interface","ICspInformation interface [Security]","GetDefaultSecurityDescriptor method","ICspInformation.GetDefaultSecurityDescriptor","ICspInformation::GetDefaultSecurityDescriptor","certenroll/ICspInformation::GetDefaultSecurityDescriptor","security.icspinformation_getdefaultsecuritydescriptor"]
old-location: security\icspinformation_getdefaultsecuritydescriptor.htm
tech.root: security
ms.assetid: b4594400-29f2-47e2-8b4f-87ee82ea5e82
ms.date: 12/05/2018
ms.keywords: GetDefaultSecurityDescriptor, GetDefaultSecurityDescriptor method [Security], GetDefaultSecurityDescriptor method [Security],ICspInformation interface, ICspInformation interface [Security],GetDefaultSecurityDescriptor method, ICspInformation.GetDefaultSecurityDescriptor, ICspInformation::GetDefaultSecurityDescriptor, certenroll/ICspInformation::GetDefaultSecurityDescriptor, security.icspinformation_getdefaultsecuritydescriptor
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspInformation::GetDefaultSecurityDescriptor
 - certenroll/ICspInformation::GetDefaultSecurityDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformation.GetDefaultSecurityDescriptor
---

# ICspInformation::GetDefaultSecurityDescriptor


## -description

The <b>GetDefaultSecurityDescriptor</b> method retrieves the default private key security descriptor.

## -parameters

### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that indicates whether to retrieve the security descriptor for the computer or the user. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.

### -param pValue [out]

Pointer to a  <b>BSTR</b> variable that contains the security descriptor.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The property value could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The cryptographic provider does not support security descriptors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_FOUND</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The cryptographic provider does not support security descriptors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY_STATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The cryptographic provider does not support security descriptors.

</td>
</tr>
</table>

## -remarks

To use the security descriptor, you must call the <a href="/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora">ConvertStringSecurityDescriptorToSecurityDescriptor</a> function included with the Microsoft Authorization API and specify the string returned by the <b>GetDefaultSecurityDescriptor</b> method. The function returns a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

The default security descriptor is used to define access to private keys for the computer and user in the following manner:<ul>
<li>By default, only local administrators and services running under the LocalSystem account can access private keys associated with the computer account.</li>
<li>When a provider stores the private key of a user in an encrypted file in the user profile, it uses a security descriptor to set access permissions to the file.</li>
</ul>


This method retrieves the default security descriptor that will be associated with the specified <i>MachineContext</i> parameter and the current provider if a new private key is created.  You can use the default descriptor to create a custom descriptor. Custom descriptors are typically created when a private key associated with a computer context certificate must be used by a service running under an account other than the LocalSystem account.

Some cryptographic providers do not support security descriptors. Examples include smart card and hardware security module (HSM) providers.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>