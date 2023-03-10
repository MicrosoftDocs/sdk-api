---
UID: NF:certenroll.IX509PrivateKey.get_ReaderName
title: IX509PrivateKey::get_ReaderName (certenroll.h)
description: Specifies or retrieves the name of a smart card reader. (Get)
helpviewer_keywords: ["IX509PrivateKey interface [Security]","ReaderName property","IX509PrivateKey.ReaderName","IX509PrivateKey.get_ReaderName","IX509PrivateKey::ReaderName","IX509PrivateKey::get_ReaderName","IX509PrivateKey::put_ReaderName","ReaderName property [Security]","ReaderName property [Security]","IX509PrivateKey interface","certenroll/IX509PrivateKey::ReaderName","certenroll/IX509PrivateKey::get_ReaderName","certenroll/IX509PrivateKey::put_ReaderName","get_ReaderName","security.ix509privatekey_readername_property"]
old-location: security\ix509privatekey_readername_property.htm
tech.root: security
ms.assetid: 1c9bb81a-c91b-42b9-a44c-de1ae5b68af6
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],ReaderName property, IX509PrivateKey.ReaderName, IX509PrivateKey.get_ReaderName, IX509PrivateKey::ReaderName, IX509PrivateKey::get_ReaderName, IX509PrivateKey::put_ReaderName, ReaderName property [Security], ReaderName property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::ReaderName, certenroll/IX509PrivateKey::get_ReaderName, certenroll/IX509PrivateKey::put_ReaderName, get_ReaderName, security.ix509privatekey_readername_property
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
 - IX509PrivateKey::get_ReaderName
 - certenroll/IX509PrivateKey::get_ReaderName
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
 - IX509PrivateKey.ReaderName
 - IX509PrivateKey.get_ReaderName
 - IX509PrivateKey.put_ReaderName
---

# IX509PrivateKey::get_ReaderName


## -description

The <b>ReaderName</b> property specifies or retrieves the name of a smart card reader.

This property is read/write.

## -parameters

## -remarks

If you set this property before opening a key, the reader name is concatenated to the name of the key container. The format is \\.&#92;<i>Reader_Name</i>&#92;<i>Container_Name</i>. Prepending the reader name to the key container name enables the name to be disambiguated in subsequent calls to a cryptographic provider. The private key is typically stored in the smart card key container when a smart card is used.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
