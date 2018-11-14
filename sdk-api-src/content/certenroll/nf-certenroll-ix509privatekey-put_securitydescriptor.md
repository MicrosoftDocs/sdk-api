---
UID: NF:certenroll.IX509PrivateKey.put_SecurityDescriptor
title: IX509PrivateKey::put_SecurityDescriptor
author: windows-sdk-content
description: Specifies or retrieves the security descriptor for the private key.
old-location: security\ix509privatekey_securitydescriptor_property.htm
tech.root: SecCertEnroll
ms.assetid: 5fa1e5d8-b745-494c-a727-426084fce2a1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509PrivateKey interface [Security],SecurityDescriptor property, IX509PrivateKey.SecurityDescriptor, IX509PrivateKey.put_SecurityDescriptor, IX509PrivateKey::SecurityDescriptor, IX509PrivateKey::get_SecurityDescriptor, IX509PrivateKey::put_SecurityDescriptor, SecurityDescriptor property [Security], SecurityDescriptor property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::SecurityDescriptor, certenroll/IX509PrivateKey::get_SecurityDescriptor, certenroll/IX509PrivateKey::put_SecurityDescriptor, put_SecurityDescriptor, security.ix509privatekey_securitydescriptor_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509PrivateKey.put_SecurityDescriptor
: 
---

# IX509PrivateKey::put_SecurityDescriptor


## -description


The <b>SecurityDescriptor</b> property specifies or retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.

This property is read/write.


## -parameters


## -remarks



To use the security descriptor, you must call the <a href="https://msdn.microsoft.com/c5654148-fb4c-436d-9378-a1168fc82607">ConvertStringSecurityDescriptorToSecurityDescriptor</a> function included with the Microsoft Authorization API and specify the string returned by the <a href="https://msdn.microsoft.com/b4594400-29f2-47e2-8b4f-87ee82ea5e82">GetDefaultSecurityDescriptor</a> method.

The security descriptor is used to define access to private keys for the computer and user in the following manner:<ul>
<li>By default, only local administrators and services running under the LocalSystem account can access private keys associated with the computer account.</li>
<li>When a CSP stores the private key of a user in an encrypted file in the user profile, it uses a security descriptor to set access permissions to the file.</li>
</ul>


If the key is not open when you specify a descriptor, the property value  will be set when the key is opened.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

