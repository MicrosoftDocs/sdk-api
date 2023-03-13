---
UID: NE:certenroll.RequestClientInfoClientId
title: RequestClientInfoClientId (certenroll.h)
description: Specifies the type of application that created a certificate request.
helpviewer_keywords: ["ClientIdAutoEnroll","ClientIdAutoEnroll2003","ClientIdCertReq","ClientIdCertReq2003","ClientIdDefaultRequest","ClientIdEOBO","ClientIdNone","ClientIdRequestWizard","ClientIdTest","ClientIdUserStart","ClientIdWizard2003","ClientIdXEnroll2003","RequestClientInfoClientId","RequestClientInfoClientId enumeration [Security]","certenroll/ClientIdAutoEnroll","certenroll/ClientIdAutoEnroll2003","certenroll/ClientIdCertReq","certenroll/ClientIdCertReq2003","certenroll/ClientIdDefaultRequest","certenroll/ClientIdEOBO","certenroll/ClientIdNone","certenroll/ClientIdRequestWizard","certenroll/ClientIdTest","certenroll/ClientIdUserStart","certenroll/ClientIdWizard2003","certenroll/ClientIdXEnroll2003","certenroll/RequestClientInfoClientId","security.requestclientinfoclientid_enum"]
old-location: security\requestclientinfoclientid_enum.htm
tech.root: security
ms.assetid: 0c9ee81d-105d-4e97-9de3-169ff77e55f0
ms.date: 12/05/2018
ms.keywords: ClientIdAutoEnroll, ClientIdAutoEnroll2003, ClientIdCertReq, ClientIdCertReq2003, ClientIdDefaultRequest, ClientIdEOBO, ClientIdNone, ClientIdRequestWizard, ClientIdTest, ClientIdUserStart, ClientIdWizard2003, ClientIdXEnroll2003, RequestClientInfoClientId, RequestClientInfoClientId enumeration [Security], certenroll/ClientIdAutoEnroll, certenroll/ClientIdAutoEnroll2003, certenroll/ClientIdCertReq, certenroll/ClientIdCertReq2003, certenroll/ClientIdDefaultRequest, certenroll/ClientIdEOBO, certenroll/ClientIdNone, certenroll/ClientIdRequestWizard, certenroll/ClientIdTest, certenroll/ClientIdUserStart, certenroll/ClientIdWizard2003, certenroll/ClientIdXEnroll2003, certenroll/RequestClientInfoClientId, security.requestclientinfoclientid_enum
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RequestClientInfoClientId
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RequestClientInfoClientId
 - certenroll/RequestClientInfoClientId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - RequestClientInfoClientId
---

# RequestClientInfoClientId enumeration


## -description

The <b>RequestClientInfoClientId</b> enumeration  specifies the type of application that created a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.  This can be used to initialize a <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a> object that contains information about the client. It is also used by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface.

## -enum-fields

### -field ClientIdNone:0

No client identifier is specified.

### -field ClientIdXEnroll2003:1

Specifies the Certificate Enrollment Control that is available on Windows Server 2003.

### -field ClientIdAutoEnroll2003:2

Specifies the autoenrollment  that is available on Windows Server 2003.

### -field ClientIdWizard2003:3

Specifies the Certificate Request Wizard that is available on Windows Server 2003.

### -field ClientIdCertReq2003:4

Specifies the Certreq.exe command-line tool that is available on Windows Server 2003.

### -field ClientIdDefaultRequest:5

Specifies the default certificate request object that is available starting with Windows Vista. This is represented by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface and is the default value if the client ID is not set by the caller.

### -field ClientIdAutoEnroll:6

Specifies the autoenrollment that is available starting with  Windows Vista.

### -field ClientIdRequestWizard:7

Specifies the Certificate Request Wizard that is available starting with Windows Vista.

### -field ClientIdEOBO:8

Specifies the Enroll-On-Behalf-Of (EOBO) Wizard that is available starting with Windows Vista.

### -field ClientIdCertReq:9

Specifies the Certreq.exe command-line tool that is available starting with Windows Vista.

### -field ClientIdTest:10

This value is not supported.

### -field ClientIdWinRT:11

### -field ClientIdUserStart:1000

This is the base value for custom applications.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>
