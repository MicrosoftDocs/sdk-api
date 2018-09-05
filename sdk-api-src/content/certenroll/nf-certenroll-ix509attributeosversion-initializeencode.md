---
UID: NF:certenroll.IX509AttributeOSVersion.InitializeEncode
title: IX509AttributeOSVersion::InitializeEncode
author: windows-sdk-content
description: Initializes the attribute from operating system version information.
old-location: security\ix509attributeosversioner_initializeencode_method.htm
old-project: SecCertEnroll
ms.assetid: 1eee63f8-8345-4f3d-9fee-d8d67bcebb8c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509AttributeOSVersion interface [Security],InitializeEncode method, IX509AttributeOSVersion.InitializeEncode, IX509AttributeOSVersion::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeOSVersion interface, certenroll/IX509AttributeOSVersion::InitializeEncode, security.ix509attributeosversioner_initializeencode_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeOSVersion.InitializeEncode
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeOSVersion::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the attribute from operating system version information.


## -parameters




### -param strOSVersion [in, optional]

A <b>BSTR</b> variable that contains the version information. The format of the string is <i>major.minor.build.platform</i>. This parameter is optional. If you do not specify a string, this method calls the <b>GetVersionEx</b> function.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for this attribute is <b>XCN_OID_OS_VERSION</b> (1.3.6.1.4.1.311.13.2.3). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/2f13002f-bdaa-4c82-859a-da932615dd81">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/2ae84d47-2bda-4954-9165-902634d09da9">IX509AttributeOSVersion</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="https://msdn.microsoft.com/395ec2be-fe92-4bf1-bed3-db122e22f15e">OSVersion</a> property to retrieve the raw data.




## -see-also




<a href="https://msdn.microsoft.com/2ae84d47-2bda-4954-9165-902634d09da9">IX509AttributeOSVersion</a>
 

 

