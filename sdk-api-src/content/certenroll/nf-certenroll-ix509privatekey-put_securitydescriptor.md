---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

