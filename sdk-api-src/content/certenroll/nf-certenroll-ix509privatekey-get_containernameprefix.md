---
UID: NF:certenroll.IX509PrivateKey.get_ContainerNamePrefix
title: IX509PrivateKey::get_ContainerNamePrefix
author: windows-sdk-content
description: Specifies or retrieves a prefix added to the name of the key container.
old-location: security\ix509privatekey_containernameprefix.htm
tech.root: seccertenroll
ms.assetid: af5a30dd-4707-4b38-bf6b-b971d854d5b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContainerNamePrefix property [Security], ContainerNamePrefix property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],ContainerNamePrefix property, IX509PrivateKey.ContainerNamePrefix, IX509PrivateKey.get_ContainerNamePrefix, IX509PrivateKey::ContainerNamePrefix, IX509PrivateKey::get_ContainerNamePrefix, IX509PrivateKey::put_ContainerNamePrefix, certenroll/IX509PrivateKey::ContainerNamePrefix, certenroll/IX509PrivateKey::get_ContainerNamePrefix, certenroll/IX509PrivateKey::put_ContainerNamePrefix, get_ContainerNamePrefix, security.ix509privatekey_containernameprefix
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
 - IX509PrivateKey.ContainerNamePrefix
 - IX509PrivateKey.get_ContainerNamePrefix
 - IX509PrivateKey.put_ContainerNamePrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::get_ContainerNamePrefix


## -description


The <b>ContainerNamePrefix</b> property specifies or retrieves a prefix added to the name of the key container.

This property is read/write.


## -parameters


## -remarks



A prefix can contain any string limited to the maximum length of the key container name and to legal container name characters. For example, if you do not call the <a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a> property to specify a key container name, one is automatically created when the <a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a> method is called, and the prefix to the container name will be the string "lp". For another example, if you are creating a test harness and want to differentiate key containers by the programs that generated them, you can use the name of the executable as the prefix.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

