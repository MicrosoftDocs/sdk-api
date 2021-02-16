---
UID: NS:wincrypt._CRYPT_TIMESTAMP_ACCURACY
title: CRYPT_TIMESTAMP_ACCURACY (wincrypt.h)
description: Is used by the CRYPT_TIMESTAMP_INFO structure to represent the accuracy of the time deviation around the UTC time at which the time stamp token was created by the Time Stamp Authority (TSA).
helpviewer_keywords: ["*PCRYPT_TIMESTAMP_ACCURACY","CRYPT_TIMESTAMP_ACCURACY","CRYPT_TIMESTAMP_ACCURACY structure [Security]","PCRYPT_TIMESTAMP_ACCURACY","PCRYPT_TIMESTAMP_ACCURACY structure pointer [Security]","security.crypt_timestamp_accuracy","wincrypt/CRYPT_TIMESTAMP_ACCURACY","wincrypt/PCRYPT_TIMESTAMP_ACCURACY"]
old-location: security\crypt_timestamp_accuracy.htm
tech.root: security
ms.assetid: 9115db8a-7cc1-4360-b89b-6c33ddb67fe9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIMESTAMP_ACCURACY, CRYPT_TIMESTAMP_ACCURACY, CRYPT_TIMESTAMP_ACCURACY structure [Security], PCRYPT_TIMESTAMP_ACCURACY, PCRYPT_TIMESTAMP_ACCURACY structure pointer [Security], security.crypt_timestamp_accuracy, wincrypt/CRYPT_TIMESTAMP_ACCURACY, wincrypt/PCRYPT_TIMESTAMP_ACCURACY'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_TIMESTAMP_ACCURACY, *PCRYPT_TIMESTAMP_ACCURACY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIMESTAMP_ACCURACY
 - wincrypt/_CRYPT_TIMESTAMP_ACCURACY
 - PCRYPT_TIMESTAMP_ACCURACY
 - wincrypt/PCRYPT_TIMESTAMP_ACCURACY
 - CRYPT_TIMESTAMP_ACCURACY
 - wincrypt/CRYPT_TIMESTAMP_ACCURACY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_TIMESTAMP_ACCURACY
---

# CRYPT_TIMESTAMP_ACCURACY structure


## -description

The <b>CRYPT_TIMESTAMP_ACCURACY</b> structure is used by the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_info">CRYPT_TIMESTAMP_INFO</a> structure to represent the accuracy of the time deviation around the UTC time at which the time stamp token was created by the Time Stamp Authority (TSA).

## -struct-fields

### -field dwSeconds

Optional. Specifies, in seconds, the accuracy of the upper limit of the time at which the time stamp token was created by the TSA.

### -field dwMillis

Optional. Specifies, in milliseconds, the accuracy of the upper limit of the time at which the time stamp token was  created by the TSA.

### -field dwMicros

Optional. Specifies, in microseconds, the accuracy of the upper limit of the time at which the time-stamp token was created by the TSA.