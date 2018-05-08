---
UID: NF:certenroll.IBinaryConverter.StringToString
title: IBinaryConverter::StringToString
author: windows-driver-content
description: Modifies the type of Unicode encoding applied to a string.
old-location: security\ibinaryconverter_stringtostring_method.htm
old-project: SecCertEnroll
ms.assetid: c584a9bd-4ea3-4df7-8a9a-1f70cf07a213
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IBinaryConverter interface [Security],StringToString method, IBinaryConverter.StringToString, IBinaryConverter::StringToString, StringToString, StringToString method [Security], StringToString method [Security],IBinaryConverter interface, certenroll/IBinaryConverter::StringToString, security.ibinaryconverter_stringtostring_method
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
-	IBinaryConverter.StringToString
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IBinaryConverter::StringToString


## -description


The <b>StringToString</b> method modifies the type of Unicode encoding applied to a string.


## -parameters




### -param strEncodedIn [in]

A <b>BSTR</b> variable that contains the string to modify.


### -param EncodingIn [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the Unicode encoding applied to  the input string.


### -param Encoding [in]

An  <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode encoding to apply to the output string. The default value is <b>XCN_CRYPT_STRING_BASE64</b>.


### -param pstrEncoded [out]

Pointer to a <b>BSTR</b> variable that contains the encoded output string.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/495a321a-3005-4537-b082-5003e437d21f">IBinaryConverter</a>
 

 

