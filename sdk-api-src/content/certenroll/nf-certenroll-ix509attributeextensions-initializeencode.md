---
UID: NF:certenroll.IX509AttributeExtensions.InitializeEncode
title: IX509AttributeExtensions::InitializeEncode
author: windows-sdk-content
description: Initializes the object from an IX509Extensions collection.
old-location: security\ix509attributeextensions_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: f5b6f0b9-ca49-42f2-842c-34c2445c3824
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509AttributeExtensions interface [Security],InitializeEncode method, IX509AttributeExtensions.InitializeEncode, IX509AttributeExtensions::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeExtensions interface, certenroll/IX509AttributeExtensions::InitializeEncode, security.ix509attributeextensions_initializeencode_method
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
 - IX509AttributeExtensions.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeExtensions::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the object from an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection.


## -parameters




### -param pExtensions [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> interface that contains the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> for this attribute is <b>XCN_OID_RSA_certExtensions</b> (1.2.840.113549.1.9.14). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa377091(v=VS.85).aspx">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure that contains the certificate extensions. You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa377095(v=VS.85).aspx">X509Extensions</a> property to retrieve the extensions.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377058(v=VS.85).aspx">IX509Attribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377108(v=VS.85).aspx">IX509Attributes</a>
 

 

