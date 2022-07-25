---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModuleSession.GenerateRequest
title: IMFContentDecryptionModuleSession::GenerateRequest
ms.date: 11/26/2019
targetos: Windows
description: Generates a license request based on the provided data.
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
 - IMFContentDecryptionModuleSession::GenerateRequest
f1_keywords:
 - IMFContentDecryptionModuleSession::GenerateRequest
 - mfcontentdecryptionmodule/IMFContentDecryptionModuleSession::GenerateRequest
dev_langs:
 - c++
---

## -description

Generates a license request based on the provided data.

## -parameters

### -param initDataType

A **LPCWSTR** specifying the type of the data provided in the *initData* parameter. The string format is specified by the Encrypted Media Extension specification's [Initialization Data Type](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#initialization-data-type).

### -param initData

A **BYTE** array containing initialization data. The data format is specified by the Encrypted Media Extension specification's [Initialization Data](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#initialization-data).

### -param initDataSize

The size of the **BYTE** array provided in the *initData* parameter.

## -returns

Returns S_OK on success.

## -remarks

**GenerateRequest** is based on the Encrypted Media Extension specification's [MediaKeySession.generateRequest](https://www.w3.org/TR/2017/REC-encrypted-media-20170918/#dom-mediakeysession-generaterequest).

## -see-also

