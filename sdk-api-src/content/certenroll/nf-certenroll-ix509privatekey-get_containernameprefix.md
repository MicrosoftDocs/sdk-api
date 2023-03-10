---
UID: NF:certenroll.IX509PrivateKey.get_ContainerNamePrefix
title: IX509PrivateKey::get_ContainerNamePrefix (certenroll.h)
description: Specifies or retrieves a prefix added to the name of the key container. (Get)
helpviewer_keywords: ["ContainerNamePrefix property [Security]","ContainerNamePrefix property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","ContainerNamePrefix property","IX509PrivateKey.ContainerNamePrefix","IX509PrivateKey.get_ContainerNamePrefix","IX509PrivateKey::ContainerNamePrefix","IX509PrivateKey::get_ContainerNamePrefix","IX509PrivateKey::put_ContainerNamePrefix","certenroll/IX509PrivateKey::ContainerNamePrefix","certenroll/IX509PrivateKey::get_ContainerNamePrefix","certenroll/IX509PrivateKey::put_ContainerNamePrefix","get_ContainerNamePrefix","security.ix509privatekey_containernameprefix"]
old-location: security\ix509privatekey_containernameprefix.htm
tech.root: security
ms.assetid: af5a30dd-4707-4b38-bf6b-b971d854d5b0
ms.date: 12/05/2018
ms.keywords: ContainerNamePrefix property [Security], ContainerNamePrefix property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],ContainerNamePrefix property, IX509PrivateKey.ContainerNamePrefix, IX509PrivateKey.get_ContainerNamePrefix, IX509PrivateKey::ContainerNamePrefix, IX509PrivateKey::get_ContainerNamePrefix, IX509PrivateKey::put_ContainerNamePrefix, certenroll/IX509PrivateKey::ContainerNamePrefix, certenroll/IX509PrivateKey::get_ContainerNamePrefix, certenroll/IX509PrivateKey::put_ContainerNamePrefix, get_ContainerNamePrefix, security.ix509privatekey_containernameprefix
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
 - IX509PrivateKey::get_ContainerNamePrefix
 - certenroll/IX509PrivateKey::get_ContainerNamePrefix
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
 - IX509PrivateKey.ContainerNamePrefix
 - IX509PrivateKey.get_ContainerNamePrefix
 - IX509PrivateKey.put_ContainerNamePrefix
---

# IX509PrivateKey::get_ContainerNamePrefix


## -description

The <b>ContainerNamePrefix</b> property specifies or retrieves a prefix added to the name of the key container.

This property is read/write.

## -parameters

## -remarks

A prefix can contain any string limited to the maximum length of the key container name and to legal container name characters. For example, if you do not call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a> property to specify a key container name, one is automatically created when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> method is called, and the prefix to the container name will be the string "lp". For another example, if you are creating a test harness and want to differentiate key containers by the programs that generated them, you can use the name of the executable as the prefix.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
