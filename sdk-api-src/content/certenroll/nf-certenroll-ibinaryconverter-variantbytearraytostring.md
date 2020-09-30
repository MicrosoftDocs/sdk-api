---
UID: NF:certenroll.IBinaryConverter.VariantByteArrayToString
title: IBinaryConverter::VariantByteArrayToString (certenroll.h)
description: Creates a Unicode encoded string from a byte array.
helpviewer_keywords: ["IBinaryConverter interface [Security]","VariantByteArrayToString method","IBinaryConverter.VariantByteArrayToString","IBinaryConverter::VariantByteArrayToString","VariantByteArrayToString","VariantByteArrayToString method [Security]","VariantByteArrayToString method [Security]","IBinaryConverter interface","certenroll/IBinaryConverter::VariantByteArrayToString","security.ibinaryconverter_variantbytearraytostring_method"]
old-location: security\ibinaryconverter_variantbytearraytostring_method.htm
tech.root: security
ms.assetid: c10c93c1-10b1-4724-9df5-3c17c593c2b9
ms.date: 12/05/2018
ms.keywords: IBinaryConverter interface [Security],VariantByteArrayToString method, IBinaryConverter.VariantByteArrayToString, IBinaryConverter::VariantByteArrayToString, VariantByteArrayToString, VariantByteArrayToString method [Security], VariantByteArrayToString method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::VariantByteArrayToString, security.ibinaryconverter_variantbytearraytostring_method
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
 - IBinaryConverter::VariantByteArrayToString
 - certenroll/IBinaryConverter::VariantByteArrayToString
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
 - IBinaryConverter.VariantByteArrayToString
---

# IBinaryConverter::VariantByteArrayToString


## -description

The <b>VariantByteArrayToString</b> method creates a Unicode encoded string from a byte array.  You can use this method to create a printable string from a <a href="/windows/desktop/SecGloss/c-gly">certificate BLOB</a>.

## -parameters

### -param pvarByteArray [in]

Pointer to a  <b>VARIANT</b> array of bytes to be encoded. Each byte in the array must be an unsigned integer. That is, the VARTYPE enumeration value must equal <b>VT_ARRAY</b> | <b>VT_UI1</b>.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the Unicode encoding applied to the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.

### -param pstrEncoded [out]

Pointer to a  <b>BSTR</b> variable that contains the Unicode-encoded certificate.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a>