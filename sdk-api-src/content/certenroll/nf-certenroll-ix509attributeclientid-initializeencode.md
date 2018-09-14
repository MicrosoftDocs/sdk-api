---
UID: NF:certenroll.IX509AttributeClientId.InitializeEncode
title: IX509AttributeClientId::InitializeEncode
author: windows-sdk-content
description: Initializes the attribute from information about the user, client computer, and application that submitted the certificate request.
old-location: security\ix509attributeclientid_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: 6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509AttributeClientId interface [Security],InitializeEncode method, IX509AttributeClientId.InitializeEncode, IX509AttributeClientId::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::InitializeEncode, security.ix509attributeclientid_initializeencode_method
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
 - IX509AttributeClientId.InitializeEncode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeClientId::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the attribute from information about the user, client computer, and application that submitted the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.


## -parameters




### -param ClientId [in]

A <a href="https://msdn.microsoft.com/0c9ee81d-105d-4e97-9de3-169ff77e55f0">RequestClientInfoClientId</a> enumeration value that identifies the type of application that created the request. Examples include autoenrollment services, command-line request tools, and custom request applications.


### -param strMachineDnsName [in, optional]

A <b>BSTR</b> variable that contains the Domain Name System (DNS) name of the computer on which the request was created, for example <i>ComputerName.contoso.com</i>. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a> function. If a name cannot be found, the method fails.


### -param strUserSamName [in, optional]

A <b>BSTR</b> variable that contains the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) name for the user in the form <i>DomainName\UserName</i>. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/7e7d618b-2e64-4b0b-aed3-f3221b0443ca">GetUserNameEx</a> function. If a name cannot be found, the method fails.


### -param strProcessName [in, optional]

A <b>BSTR</b> variable that contains the name of the application that created the certificate request. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine()</a> function and parses the command line. If a name cannot be found, the method fails.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for this attribute is <b>XCN_OID_REQUEST_CLIENT_INFO</b> (1.3.6.1.4.1.311.21.20). For more information, see <a href="https://msdn.microsoft.com/30e8c740-854b-409f-a138-3871df305708">CERTENROLL_OBJECTID</a>. The attribute is created as an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure that is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/653b44fd-f69c-49e3-8aee-02445fa03cde">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/43073f84-28c6-4342-82ec-ca2289d51e02">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/596682fc-aaf4-4247-a44b-34001cf7aecb">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd">ProcessName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a5a5027f-3854-4064-9cf7-675562b4cd57">UserSamName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>
 

 

