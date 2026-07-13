---
UID: NF:certenroll.IX509PrivateKey.put_ContainerName
title: IX509PrivateKey::put_ContainerName (certenroll.h)
description: Specifies or retrieves the name of the key container. (Put)
helpviewer_keywords: ["ContainerName property [Security]","ContainerName property [Security]","IX509PrivateKey interface","IX509PrivateKey interface [Security]","ContainerName property","IX509PrivateKey.ContainerName","IX509PrivateKey.put_ContainerName","IX509PrivateKey::ContainerName","IX509PrivateKey::get_ContainerName","IX509PrivateKey::put_ContainerName","certenroll/IX509PrivateKey::ContainerName","certenroll/IX509PrivateKey::get_ContainerName","certenroll/IX509PrivateKey::put_ContainerName","put_ContainerName","security.ix509privatekey_containername_property"]
old-location: security\ix509privatekey_containername_property.htm
tech.root: security
ms.assetid: 1d56fa7e-8113-461d-a4f0-ebc048fbcb49
ms.date: 12/05/2018
ms.keywords: ContainerName property [Security], ContainerName property [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],ContainerName property, IX509PrivateKey.ContainerName, IX509PrivateKey.put_ContainerName, IX509PrivateKey::ContainerName, IX509PrivateKey::get_ContainerName, IX509PrivateKey::put_ContainerName, certenroll/IX509PrivateKey::ContainerName, certenroll/IX509PrivateKey::get_ContainerName, certenroll/IX509PrivateKey::put_ContainerName, put_ContainerName, security.ix509privatekey_containername_property
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
 - IX509PrivateKey::put_ContainerName
 - certenroll/IX509PrivateKey::put_ContainerName
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
 - IX509PrivateKey.ContainerName
 - IX509PrivateKey.get_ContainerName
 - IX509PrivateKey.put_ContainerName
---

# IX509PrivateKey::put_ContainerName


## -description

The <b>ContainerName</b> property specifies or retrieves the name of the key container. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

If you do not specify a name, one is created when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a> method is called.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
