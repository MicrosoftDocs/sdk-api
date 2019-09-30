---
UID: NF:certenroll.IX509AttributeClientId.InitializeEncode
title: IX509AttributeClientId::InitializeEncode (certenroll.h)
author: windows-sdk-content
description: Initializes the attribute from information about the user, client computer, and application that submitted the certificate request.
old-location: security\ix509attributeclientid_initializeencode_method.htm
tech.root: seccertenroll
ms.assetid: 6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId interface [Security],InitializeEncode method, IX509AttributeClientId.InitializeEncode, IX509AttributeClientId::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::InitializeEncode, security.ix509attributeclientid_initializeencode_method
ms.topic: method
f1_keywords: 
 - "certenroll/IX509AttributeClientId.InitializeEncode"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509AttributeClientId::InitializeEncode


## -description


The <b>InitializeEncode</b> method initializes the attribute from information about the user, client computer, and application that submitted the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>.


## -parameters




### -param ClientId [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-requestclientinfoclientid">RequestClientInfoClientId</a> enumeration value that identifies the type of application that created the request. Examples include autoenrollment services, command-line request tools, and custom request applications.


### -param strMachineDnsName [in, optional]

A <b>BSTR</b> variable that contains the Domain Name System (DNS) name of the computer on which the request was created, for example <i>ComputerName.contoso.com</i>. If you do not supply a name, the method calls the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a> function. If a name cannot be found, the method fails.


### -param strUserSamName [in, optional]

A <b>BSTR</b> variable that contains the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) name for the user in the form <i>DomainName\UserName</i>. If you do not supply a name, the method calls the <a href="https://docs.microsoft.com/windows/desktop/api/secext/nf-secext-getusernameexa">GetUserNameEx</a> function. If a name cannot be found, the method fails.


### -param strProcessName [in, optional]

A <b>BSTR</b> variable that contains the name of the application that created the certificate request. If you do not supply a name, the method calls the <a href="https://docs.microsoft.com/windows/desktop/api/processenv/nf-processenv-getcommandlinea">GetCommandLine()</a> function and parses the command line. If a name cannot be found, the method fails.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_REQUEST_CLIENT_INFO</b> (1.3.6.1.4.1.311.21.20). For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>. The attribute is created as an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure that is encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

You must call either <b>InitializeEncode</b> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a> before you can use an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_machinednsname">MachineDnsName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_processname">ProcessName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_usersamname">UserSamName</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>
 

 

