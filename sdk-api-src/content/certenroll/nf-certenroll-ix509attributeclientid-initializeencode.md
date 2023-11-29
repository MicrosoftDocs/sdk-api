---
UID: NF:certenroll.IX509AttributeClientId.InitializeEncode
title: IX509AttributeClientId::InitializeEncode (certenroll.h)
description: Initializes the attribute from information about the user, client computer, and application that submitted the certificate request.
helpviewer_keywords: ["IX509AttributeClientId interface [Security]","InitializeEncode method","IX509AttributeClientId.InitializeEncode","IX509AttributeClientId::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509AttributeClientId interface","certenroll/IX509AttributeClientId::InitializeEncode","security.ix509attributeclientid_initializeencode_method"]
old-location: security\ix509attributeclientid_initializeencode_method.htm
tech.root: security
ms.assetid: 6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd
ms.date: 11/27/2023
ms.keywords: IX509AttributeClientId interface [Security],InitializeEncode method, IX509AttributeClientId.InitializeEncode, IX509AttributeClientId::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeClientId interface, certenroll/IX509AttributeClientId::InitializeEncode, security.ix509attributeclientid_initializeencode_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509AttributeClientId::InitializeEncode
 - certenroll/IX509AttributeClientId::InitializeEncode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeClientId.InitializeEncode
---

# IX509AttributeClientId::InitializeEncode

## -description

The **InitializeEncode** method initializes the attribute from information about the user, client computer, and application that submitted the [certificate request](/windows/win32/SecGloss/c-gly).

## -parameters

### -param ClientId [in]

A [RequestClientInfoClientId](/windows/win32/api/certenroll/ne-certenroll-requestclientinfoclientid) enumeration value that identifies the type of application that created the request. Examples include auto-enrollment services, command-line request tools, and custom request applications.

### -param strMachineDnsName [in, optional]

A **BSTR** variable that contains the Domain Name System (DNS) name of the computer on which the request was created, for example `ComputerName.contoso.com`. If you do not supply a name, the method calls the [GetComputerNameEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function. If a name cannot be found, the method fails.

### -param strUserSamName [in, optional]

A **BSTR** variable that contains the [Security Accounts Manager](/windows/win32/SecGloss/s-gly) (SAM) name for the user in the form *DomainName\UserName*. If you do not supply a name, the method calls the [GetUserNameEx](/windows/win32/api/secext/nf-secext-getusernameexa) function. If a name cannot be found, the method fails.

### -param strProcessName [in, optional]

A **BSTR** variable that contains the name of the application that created the certificate request. If you do not supply a name, the method calls the [GetCommandLine](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) function and parses the command line. If a name cannot be found, the method fails.

## -returns

If the function succeeds, the function returns **S_OK**.

If the function fails, it returns an **HRESULT** value that indicates the error. For a list of common error codes, see [Common HRESULT Values](/windows/win32/SecCrypto/common-hresult-values).

## -remarks

The [object identifier](/windows/win32/SecGloss/o-gly) (OID) for this attribute is **XCN_OID_REQUEST_CLIENT_INFO** (1.3.6.1.4.1.311.21.20). For more information, see [CERTENROLL_OBJECTID](/windows/win32/api/certenroll/ne-certenroll-certenroll_objectid). The attribute is created as an [Abstract Syntax Notation One](/windows/win32/SecGloss/a-gly) (ASN.1) structure that is encoded by using [Distinguished Encoding Rules](/windows/win32/SecGloss/d-gly) (DER).

You must call either **InitializeEncode** or [InitializeDecode](nf-certenroll-ix509attributeclientid-initializedecode.md) before you can use an [IX509AttributeClientId](nn-certenroll-ix509attributeclientid.md) object. The two methods complement each other. The **InitializeEncode** method enables you to construct an encoded ASN.1 structure from raw data, and the **InitializeDecode** method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:

- [ClientId](nf-certenroll-ix509attributeclientid-get_clientid.md)
- [MachineDnsName](nf-certenroll-ix509attributeclientid-get_machinednsname.md)
- [ProcessName](nf-certenroll-ix509attributeclientid-get_processname.md)
- [UserSamName](nf-certenroll-ix509attributeclientid-get_usersamname.md)

## -see-also

[IX509AttributeClientId](nn-certenroll-ix509attributeclientid.md)

[InitializeDecode](nf-certenroll-ix509attributeclientid-initializedecode.md)