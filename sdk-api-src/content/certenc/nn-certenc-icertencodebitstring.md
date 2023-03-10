---
UID: NN:certenc.ICertEncodeBitString
title: ICertEncodeBitString (certenc.h)
description: Provides methods for handling bit strings used in certificate extensions.
helpviewer_keywords: ["ICertEncodeBitString","ICertEncodeBitString interface [Security]","ICertEncodeBitString interface [Security]","described","_certsrv_icertencodebitstring","certenc/ICertEncodeBitString","security.icertencodebitstring"]
old-location: security\icertencodebitstring.htm
tech.root: security
ms.assetid: 51178b67-46da-49f8-9bd7-a500e846e0a8
ms.date: 12/05/2018
ms.keywords: ICertEncodeBitString, ICertEncodeBitString interface [Security], ICertEncodeBitString interface [Security],described, _certsrv_icertencodebitstring, certenc/ICertEncodeBitString, security.icertencodebitstring
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
 - ICertEncodeBitString
 - certenc/ICertEncodeBitString
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
 - ICertEncodeBitString
---

# ICertEncodeBitString interface


## -description

The <b>ICertEncodeBitString</b> interface provides methods for handling bit strings used in certificate extensions. A certificate extension can be created by using a bit string stored in an 
<a href="/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object instantiated by the 
<a href="/windows/desktop/SecCrypto/policy-modules">policy module</a>. The bit string can contain an arbitrary string of binary values. This interface is useful for encoding and decoding szOID_KEY_USAGE "2.5.29.15" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeBitString</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeBitString</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertEncodeBitString</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeBitString</b> also has these types of members:

