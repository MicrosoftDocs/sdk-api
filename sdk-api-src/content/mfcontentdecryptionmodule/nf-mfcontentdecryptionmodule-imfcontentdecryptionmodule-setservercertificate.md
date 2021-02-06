---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.SetServerCertificate
title: IMFContentDecryptionModule::SetServerCertificate
ms.date: 11/26/2019
targetos: Windows
description: Provides a server certificate to be used to encrypt messages to the license server.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfcontentdecryptionmodule.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfcontentdecryptionmodule.h
api_name:
 - IMFContentDecryptionModule::SetServerCertificate
f1_keywords:
 - IMFContentDecryptionModule::SetServerCertificate
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::SetServerCertificate
dev_langs:
 - c++
---

## -description

Provides a server certificate to be used to encrypt messages to the license server.

## -parameters

### -param certificate

A **BYTE** array containing the certificate.

### -param certificateSize

The size of the array in *certificate*.

## -returns

Returns S_OK on success.

## -remarks

**SetServerCertificate** is based on the Encrypted Media Extension specification's [SetServerCertificate](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeys-setservercertificate).

## -see-also

