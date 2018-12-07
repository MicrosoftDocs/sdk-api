---
UID: NF:certenroll.IBinaryConverter.StringToVariantByteArray
title: IBinaryConverter::StringToVariantByteArray
author: windows-sdk-content
description: Creates a byte array from a Unicode encoded string.
old-location: security\ibinaryconverter_stringtovariantbytearray_method.htm
tech.root: seccertenroll
ms.assetid: b0d649f7-79a1-452c-a790-b6c05ccb84b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBinaryConverter interface [Security],StringToVariantByteArray method, IBinaryConverter.StringToVariantByteArray, IBinaryConverter::StringToVariantByteArray, StringToVariantByteArray, StringToVariantByteArray method [Security], StringToVariantByteArray method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::StringToVariantByteArray, security.ibinaryconverter_stringtovariantbytearray_method
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
 - IBinaryConverter.StringToVariantByteArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBinaryConverter::StringToVariantByteArray


## -description


The <b>StringToVariantByteArray</b> method creates a byte array from a Unicode encoded string. Use this method to create a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate BLOB</a> from an encoded string that contains a certificate.


## -parameters




### -param strEncoded [in]

A <b>BSTR</b> variable that contains the Unicode encoded string.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the Unicode encoding applied to the input string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pvarByteArray [out]

Pointer to a  <b>VARIANT</b> array of bytes. The VARTYPE enumeration value equals <b>VT_ARRAY</b> | <b>VT_UI1</b>.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375047(v=VS.85).aspx">IBinaryConverter</a>
 

 

