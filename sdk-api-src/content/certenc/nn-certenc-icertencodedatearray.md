---
UID: NN:certenc.ICertEncodeDateArray
title: ICertEncodeDateArray (certenc.h)
description: Provides methods for handling Date arrays used in certificate extensions.
helpviewer_keywords: ["ICertEncodeDateArray","ICertEncodeDateArray interface [Security]","ICertEncodeDateArray interface [Security]","described","_certsrv_icertencodedatearray","certenc/ICertEncodeDateArray","security.icertencodedatearray"]
old-location: security\icertencodedatearray.htm
tech.root: security
ms.assetid: 9973c49a-d886-4cc4-b75e-7ff46f56d51c
ms.date: 12/05/2018
ms.keywords: ICertEncodeDateArray, ICertEncodeDateArray interface [Security], ICertEncodeDateArray interface [Security],described, _certsrv_icertencodedatearray, certenc/ICertEncodeDateArray, security.icertencodedatearray
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
 - ICertEncodeDateArray
 - certenc/ICertEncodeDateArray
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
 - ICertEncodeDateArray
---

# ICertEncodeDateArray interface


## -description

The <b>ICertEncodeDateArray</b> interface provides methods for handling <b>Date</b> arrays used in certificate extensions.

 A certificate extension can be created by using a <b>Date</b> array stored in an 
<a href="/windows/desktop/SecCrypto/writing-custom-extension-handlers">extension handler</a> COM object instantiated by the policy module. Each element in the array is a <b>Date</b> value.

This interface is provided mainly as a demonstration for encoding custom extensions. The Certificate Services sample programs in the Platform Software Development Kit (SDK) contain source code for this interface.

<b>ICertEncodeDateArray</b> is defined in Certenc.h. When you create your program, however, use Certsrv.h as the include file. Certenc.dll provides the <b>ICertEncodeDateArray</b> interface. The type information for this interface is also in Certencl.dll, which is shipped with the Platform SDK.

Certificate Services interfaces support both apartment-threading and free-threading models. For better throughput, free threading is recommended.

## -inheritance

The <b>ICertEncodeDateArray</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertEncodeDateArray</b> also has these types of members:

