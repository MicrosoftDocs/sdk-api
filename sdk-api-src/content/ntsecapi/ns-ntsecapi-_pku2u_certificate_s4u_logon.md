---
UID: NS:ntsecapi._PKU2U_CERTIFICATE_S4U_LOGON
title: "_PKU2U_CERTIFICATE_S4U_LOGON"
author: windows-sdk-content
description: Specifies a certificate used for S4U logon.
old-location: security\pku2u_certificate_s4u_logon.htm
old-project: SecAuthN
ms.assetid: 438b5637-d711-419a-a163-a9b014bf0662
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PPKU2U_CERTIFICATE_S4U_LOGON, PKU2U_CERTIFICATE_S4U_LOGON, PKU2U_CERTIFICATE_S4U_LOGON structure [Security], PPKU2U_CERTIFICATE_S4U_LOGON, PPKU2U_CERTIFICATE_S4U_LOGON structure pointer [Security], _PKU2U_CERTIFICATE_S4U_LOGON, ntsecapi/PKU2U_CERTIFICATE_S4U_LOGON, ntsecapi/PPKU2U_CERTIFICATE_S4U_LOGON, security.pku2u_certificate_s4u_logon"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PKU2U_CERTIFICATE_S4U_LOGON, *PPKU2U_CERTIFICATE_S4U_LOGON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - PKU2U_CERTIFICATE_S4U_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PKU2U_CERTIFICATE_S4U_LOGON structure


## -description


Specifies a certificate used for S4U logon.


## -struct-fields




### -field MessageType

A value of the <a href="https://msdn.microsoft.com/10de9dd4-0f6c-4431-a60d-9b9c60585676">PKU2U_LOGON_SUBMIT_TYPE</a> enumeration that indicates the logon type.


### -field Flags

This member is reserved. Do not use it.


### -field UserPrincipalName

The name of the user who is attempting to authenticate.


### -field DomainName

 


### -field CertificateLength

The size, in bytes, of the <b>Certificate</b> buffer.


### -field Certificate

The certificate data.


#### - UNICODE_STRING

This member is reserved. Do not use it.

