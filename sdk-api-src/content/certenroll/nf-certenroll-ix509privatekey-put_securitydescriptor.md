---
UID: NF:certenroll.IX509PrivateKey.put_SecurityDescriptor
title: IX509PrivateKey::put_SecurityDescriptor (certenroll.h)
description: Specifies or retrieves the security descriptor for the private key. (Put)
helpviewer_keywords: ["IX509PrivateKey interface [Security]","SecurityDescriptor property","IX509PrivateKey.SecurityDescriptor","IX509PrivateKey.put_SecurityDescriptor","IX509PrivateKey::SecurityDescriptor","IX509PrivateKey::get_SecurityDescriptor","IX509PrivateKey::put_SecurityDescriptor","SecurityDescriptor property [Security]","SecurityDescriptor property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::SecurityDescriptor","certenroll/IX509PrivateKey::get_SecurityDescriptor","certenroll/IX509PrivateKey::put_SecurityDescriptor","put_SecurityDescriptor","security.ix509privatekey_securitydescriptor_property"]
old-location: security\ix509privatekey_securitydescriptor_property.htm
tech.root: security
ms.assetid: 5fa1e5d8-b745-494c-a727-426084fce2a1
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],SecurityDescriptor property, IX509PrivateKey.SecurityDescriptor, IX509PrivateKey.put_SecurityDescriptor, IX509PrivateKey::SecurityDescriptor, IX509PrivateKey::get_SecurityDescriptor, IX509PrivateKey::put_SecurityDescriptor, SecurityDescriptor property [Security], SecurityDescriptor property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::SecurityDescriptor, certenroll/IX509PrivateKey::get_SecurityDescriptor, certenroll/IX509PrivateKey::put_SecurityDescriptor, put_SecurityDescriptor, security.ix509privatekey_securitydescriptor_property
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
 - IX509PrivateKey::put_SecurityDescriptor
 - certenroll/IX509PrivateKey::put_SecurityDescriptor
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
 - IX509PrivateKey.SecurityDescriptor
 - IX509PrivateKey.get_SecurityDescriptor
 - IX509PrivateKey.put_SecurityDescriptor
---

# IX509PrivateKey::put_SecurityDescriptor


## -description

The <b>SecurityDescriptor</b> property specifies or retrieves the <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> for the <a href="/windows/desktop/SecGloss/p-gly">private key</a>.

This property is read/write.

## -parameters

## -remarks

To use the security descriptor, you must call the <a href="/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora">ConvertStringSecurityDescriptorToSecurityDescriptor</a> function included with the Microsoft Authorization API and specify the string returned by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-getdefaultsecuritydescriptor">GetDefaultSecurityDescriptor</a> method.

The security descriptor is used to define access to private keys for the computer and user in the following manner:<ul>
<li>By default, only local administrators and services running under the LocalSystem account can access private keys associated with the computer account.</li>
<li>When a CSP stores the private key of a user in an encrypted file in the user profile, it uses a security descriptor to set access permissions to the file.</li>
</ul>


If the key is not open when you specify a descriptor, the property value  will be set when the key is opened.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
