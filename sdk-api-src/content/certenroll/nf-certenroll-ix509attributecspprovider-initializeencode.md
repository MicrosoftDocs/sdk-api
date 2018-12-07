---
UID: NF:certenroll.IX509AttributeCspProvider.InitializeEncode
title: IX509AttributeCspProvider::InitializeEncode
author: windows-sdk-content
description: Initializes the attribute from information about the provider.
old-location: security\ix509attributecspprovider_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: b0b45ea2-b682-4065-8624-08c34581b5ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509AttributeCspProvider interface [Security],InitializeEncode method, IX509AttributeCspProvider.InitializeEncode, IX509AttributeCspProvider::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::InitializeEncode, security.ix509attributecspprovider_initializeencode_method
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
 - IX509AttributeCspProvider.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeCspProvider::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the attribute from information about the provider.


## -parameters




### -param KeySpec [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa379409(v=VS.85).aspx">X509KeySpec</a> enumeration value that identifies whether the key pair is used for encryption or for signing.


### -param strProviderName [in]

A <b>BSTR</b> variable that contains the provider name.


### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the signature contained in the <i>strSignature</i> parameter.


### -param strSignature [in]

A <b>BSTR</b> variable that contains the provider signature.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENROLLMENT_CSP_PROVIDER</b> (1.3.6.1.4.1.311.13.2.2). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa377083(v=VS.85).aspx">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377085(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377088(v=VS.85).aspx">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377089(v=VS.85).aspx">Signature</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>
 

 

