---
UID: NF:certenroll.IBinaryConverter.VariantByteArrayToString
title: IBinaryConverter::VariantByteArrayToString
author: windows-sdk-content
description: Creates a Unicode encoded string from a byte array.
old-location: security\ibinaryconverter_variantbytearraytostring_method.htm
tech.root: seccertenroll
ms.assetid: c10c93c1-10b1-4724-9df5-3c17c593c2b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBinaryConverter interface [Security],VariantByteArrayToString method, IBinaryConverter.VariantByteArrayToString, IBinaryConverter::VariantByteArrayToString, VariantByteArrayToString, VariantByteArrayToString method [Security], VariantByteArrayToString method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::VariantByteArrayToString, security.ibinaryconverter_variantbytearraytostring_method
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IBinaryConverter.VariantByteArrayToString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBinaryConverter::VariantByteArrayToString


## -description


The <b>VariantByteArrayToString</b> method creates a Unicode encoded string from a byte array.  You can use this method to create a printable string from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate BLOB</a>.


## -parameters




### -param pvarByteArray [in]

Pointer to a  <b>VARIANT</b> array of bytes to be encoded. Each byte in the array must be an unsigned integer. That is, the VARTYPE enumeration value must equal <b>VT_ARRAY</b> | <b>VT_UI1</b>.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the Unicode encoding applied to the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pstrEncoded [out]

Pointer to a  <b>BSTR</b> variable that contains the Unicode-encoded certificate.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a>
 

 

