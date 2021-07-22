---
UID: NN:certenc.ICertEncodeCRLDistInfo
title: ICertEncodeCRLDistInfo (certenc.h)
description: Provides methods for handling certificate revocation list (CRL) distribution information arrays used in certificate extensions.
helpviewer_keywords: ["ICertEncodeCRLDistInfo","ICertEncodeCRLDistInfo interface [Security]","ICertEncodeCRLDistInfo interface [Security]","described","_certsrv_icertencodecrldistinfo","certenc/ICertEncodeCRLDistInfo","security.icertencodecrldistinfo"]
old-location: security\icertencodecrldistinfo.htm
tech.root: security
ms.assetid: e9c0053f-263f-4d7b-9356-bc33af989dbe
ms.date: 12/05/2018
ms.keywords: ICertEncodeCRLDistInfo, ICertEncodeCRLDistInfo interface [Security], ICertEncodeCRLDistInfo interface [Security],described, _certsrv_icertencodecrldistinfo, certenc/ICertEncodeCRLDistInfo, security.icertencodecrldistinfo
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
 - ICertEncodeCRLDistInfo
 - certenc/ICertEncodeCRLDistInfo
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
 - ICertEncodeCRLDistInfo
---

# ICertEncodeCRLDistInfo interface


## -description

The <b>ICertEncodeCRLDistInfo</b> interface provides methods for handling <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) distribution information arrays used in certificate extensions.

 A certificate extension can be created by using a CRL distribution information array stored in an 
<a href="/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object instantiated by the policy module. Each element in the array is a CRL distribution point structure that contains an array of names and name choices. This interface is useful for encoding and decoding szOID_CRL_DIST_POINTS "2.5.29.31" extensions; the SDK sample policy module uses this interface.

<b>ICertEncodeCRLDistInfo</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeCRLDistInfo</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform Software Development Kit (SDK).

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertEncodeCRLDistInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeCRLDistInfo</b> also has these types of members:

