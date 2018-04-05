---
UID: NF:certenroll.IBinaryConverter.StringToVariantByteArray
title: IBinaryConverter::StringToVariantByteArray method
author: windows-driver-content
description: Creates a byte array from a Unicode encoded string.
old-location: security\ibinaryconverter_stringtovariantbytearray_method.htm
old-project: SecCertEnroll
ms.assetid: b0d649f7-79a1-452c-a790-b6c05ccb84b0
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IBinaryConverter, IBinaryConverter interface [Security], StringToVariantByteArray method, IBinaryConverter::StringToVariantByteArray, StringToVariantByteArray method [Security], StringToVariantByteArray method [Security], IBinaryConverter interface, StringToVariantByteArray,IBinaryConverter.StringToVariantByteArray, certenroll/IBinaryConverter::StringToVariantByteArray, security.ibinaryconverter_stringtovariantbytearray_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IBinaryConverter.StringToVariantByteArray
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IBinaryConverter::StringToVariantByteArray method


## -description


The <b>StringToVariantByteArray</b> method creates a byte array from a Unicode encoded string. Use this method to create a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate BLOB</a> from an encoded string that contains a certificate.


## -parameters




### -param strEncoded [in]

A <b>BSTR</b> variable that contains the Unicode encoded string.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the Unicode encoding applied to the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pvarByteArray [out]

Pointer to a  <b>VARIANT</b> array of bytes. The VARTYPE enumeration value equals <b>VT_ARRAY</b> | <b>VT_UI1</b>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a>
 

 

