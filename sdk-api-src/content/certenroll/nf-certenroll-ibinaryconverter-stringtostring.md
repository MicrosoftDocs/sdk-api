---
UID: NF:certenroll.IBinaryConverter.StringToString
title: IBinaryConverter::StringToString (certenroll.h)
author: windows-sdk-content
description: Modifies the type of Unicode encoding applied to a string.
old-location: security\ibinaryconverter_stringtostring_method.htm
tech.root: seccertenroll
ms.assetid: c584a9bd-4ea3-4df7-8a9a-1f70cf07a213
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBinaryConverter interface [Security],StringToString method, IBinaryConverter.StringToString, IBinaryConverter::StringToString, StringToString, StringToString method [Security], StringToString method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::StringToString, security.ibinaryconverter_stringtostring_method
ms.topic: method
f1_keywords: 
 - "certenroll/IBinaryConverter.StringToString"
dev_langs:
 - c++
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
 - IBinaryConverter.StringToString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBinaryConverter::StringToString


## -description


The <b>StringToString</b> method modifies the type of Unicode encoding applied to a string.


## -parameters




### -param strEncodedIn [in]

A <b>BSTR</b> variable that contains the string to modify.


### -param EncodingIn [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the Unicode encoding applied to  the input string.


### -param Encoding [in]

An  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding to apply to the output string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pstrEncoded [out]

Pointer to a <b>BSTR</b> variable that contains the encoded output string.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a>
 

 

