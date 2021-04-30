---
UID: NF:certenroll.IBinaryConverter.StringToVariantByteArray
title: IBinaryConverter::StringToVariantByteArray (certenroll.h)
description: Creates a byte array from a Unicode encoded string.
helpviewer_keywords: ["IBinaryConverter interface [Security]","StringToVariantByteArray method","IBinaryConverter.StringToVariantByteArray","IBinaryConverter::StringToVariantByteArray","StringToVariantByteArray","StringToVariantByteArray method [Security]","StringToVariantByteArray method [Security]","IBinaryConverter interface","certenroll/IBinaryConverter::StringToVariantByteArray","security.ibinaryconverter_stringtovariantbytearray_method"]
old-location: security\ibinaryconverter_stringtovariantbytearray_method.htm
tech.root: security
ms.assetid: b0d649f7-79a1-452c-a790-b6c05ccb84b0
ms.date: 12/05/2018
ms.keywords: IBinaryConverter interface [Security],StringToVariantByteArray method, IBinaryConverter.StringToVariantByteArray, IBinaryConverter::StringToVariantByteArray, StringToVariantByteArray, StringToVariantByteArray method [Security], StringToVariantByteArray method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::StringToVariantByteArray, security.ibinaryconverter_stringtovariantbytearray_method
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
 - IBinaryConverter::StringToVariantByteArray
 - certenroll/IBinaryConverter::StringToVariantByteArray
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
 - IBinaryConverter.StringToVariantByteArray
---

# IBinaryConverter::StringToVariantByteArray


## -description

The <b>StringToVariantByteArray</b> method creates a byte array from a Unicode encoded string. Use this method to create a <a href="/windows/desktop/SecGloss/c-gly">certificate BLOB</a> from an encoded string that contains a certificate.

## -parameters

### -param strEncoded [in]

A <b>BSTR</b> variable that contains the Unicode encoded string.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the Unicode encoding applied to the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.

### -param pvarByteArray [out]

Pointer to a  <b>VARIANT</b> array of bytes. The VARTYPE enumeration value equals <b>VT_ARRAY</b> | <b>VT_UI1</b>.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a>