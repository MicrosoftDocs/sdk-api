---
UID: NF:certenroll.IX509AttributeOSVersion.InitializeEncode
title: IX509AttributeOSVersion::InitializeEncode (certenroll.h)
description: Initializes the attribute from operating system version information.
helpviewer_keywords: ["IX509AttributeOSVersion interface [Security]","InitializeEncode method","IX509AttributeOSVersion.InitializeEncode","IX509AttributeOSVersion::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509AttributeOSVersion interface","certenroll/IX509AttributeOSVersion::InitializeEncode","security.ix509attributeosversioner_initializeencode_method"]
old-location: security\ix509attributeosversioner_initializeencode_method.htm
tech.root: security
ms.assetid: 1eee63f8-8345-4f3d-9fee-d8d67bcebb8c
ms.date: 12/05/2018
ms.keywords: IX509AttributeOSVersion interface [Security],InitializeEncode method, IX509AttributeOSVersion.InitializeEncode, IX509AttributeOSVersion::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeOSVersion interface, certenroll/IX509AttributeOSVersion::InitializeEncode, security.ix509attributeosversioner_initializeencode_method
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
 - IX509AttributeOSVersion::InitializeEncode
 - certenroll/IX509AttributeOSVersion::InitializeEncode
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
 - IX509AttributeOSVersion.InitializeEncode
---

# IX509AttributeOSVersion::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the attribute from operating system version information.

## -parameters

### -param strOSVersion [in, optional]

A <b>BSTR</b> variable that contains the version information. The format of the string is <i>major.minor.build.platform</i>. This parameter is optional. If you do not specify a string, this method calls the <b>GetVersionEx</b> function.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_OS_VERSION</b> (1.3.6.1.4.1.311.13.2.3). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-initializedecode">InitializeDecode</a> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-get_osversion">OSVersion</a> property to retrieve the raw data.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>