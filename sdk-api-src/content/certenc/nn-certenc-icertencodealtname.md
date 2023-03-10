---
UID: NN:certenc.ICertEncodeAltName
title: ICertEncodeAltName (certenc.h)
description: Provides methods for handling alternate names used in certificate extensions.
helpviewer_keywords: ["ICertEncodeAltName","ICertEncodeAltName interface [Security]","ICertEncodeAltName interface [Security]","described","_certsrv_icertencodealtname","certenc/ICertEncodeAltName","security.icertencodealtname"]
old-location: security\icertencodealtname.htm
tech.root: security
ms.assetid: e0ecfcb0-f2ca-4e1c-a054-c83c03d55465
ms.date: 12/05/2018
ms.keywords: ICertEncodeAltName, ICertEncodeAltName interface [Security], ICertEncodeAltName interface [Security],described, _certsrv_icertencodealtname, certenc/ICertEncodeAltName, security.icertencodealtname
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeAltName
 - certenc/ICertEncodeAltName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeAltName
---

# ICertEncodeAltName interface


## -description

The <b>ICertEncodeAltName</b> interface provides methods for handling alternate names used in certificate extensions.

A certificate extension can be created using an alternate name array stored in an 
<a href="/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object. Each element in the array is a structure that contains a name string and a name choice.

This interface is useful for encoding and decoding szOID_SUBJECT_ALT_NAME2 "2.5.29.17" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeAltName</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeAltName</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertEncodeAltName</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeAltName</b> also has these types of members:

