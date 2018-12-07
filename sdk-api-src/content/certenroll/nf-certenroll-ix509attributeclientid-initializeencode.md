---
UID: NF:certenroll.IX509AttributeClientId.InitializeEncode
title: IX509AttributeClientId::InitializeEncode
author: windows-sdk-content
description: Initializes the attribute from information about the user, client computer, and application that submitted the certificate request.
old-location: security\ix509attributeclientid_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: 6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd
ms.author: windowssdkdev
ms.date: 12/5/2018
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


The <b>InitializeEncode</b> method initializes the attribute from information about the user, client computer, and application that submitted the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>.


## -parameters




### -param ClientId [in]

A <a href="https://msdn.microsoft.com/en-us/library/Aa379331(v=VS.85).aspx">RequestClientInfoClientId</a> enumeration value that identifies the type of application that created the request. Examples include autoenrollment services, command-line request tools, and custom request applications.


### -param strMachineDnsName [in, optional]

A <b>BSTR</b> variable that contains the Domain Name System (DNS) name of the computer on which the request was created, for example <i>ComputerName.contoso.com</i>. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a> function. If a name cannot be found, the method fails.


### -param strUserSamName [in, optional]

A <b>BSTR</b> variable that contains the <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">Security Accounts Manager</a> (SAM) name for the user in the form <i>DomainName\UserName</i>. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/en-us/library/ms724435(v=VS.85).aspx">GetUserNameEx</a> function. If a name cannot be found, the method fails.


### -param strProcessName [in, optional]

A <b>BSTR</b> variable that contains the name of the application that created the certificate request. If you do not supply a name, the method calls the <a href="https://msdn.microsoft.com/08dfcab2-eb6e-49a4-80eb-87d4076c98c6">GetCommandLine()</a> function and parses the command line. If a name cannot be found, the method fails.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for this attribute is <b>XCN_OID_REQUEST_CLIENT_INFO</b> (1.3.6.1.4.1.311.21.20). For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374855(v=VS.85).aspx">CERTENROLL_OBJECTID</a>. The attribute is created as an <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structure that is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://msdn.microsoft.com/en-us/library/Aa377075(v=VS.85).aspx">InitializeDecode</a> before you can use an <a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377074(v=VS.85).aspx">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377077(v=VS.85).aspx">MachineDnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377079(v=VS.85).aspx">ProcessName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377081(v=VS.85).aspx">UserSamName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377073(v=VS.85).aspx">IX509AttributeClientId</a>
 

 

