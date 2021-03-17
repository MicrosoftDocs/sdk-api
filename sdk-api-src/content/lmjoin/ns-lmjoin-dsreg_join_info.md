---
UID: NS:lmjoin._DSREG_JOIN_INFO
title: DSREG_JOIN_INFO (lmjoin.h)
description: Contains information about how a device is joined to Microsoft Azure Active Directory.
helpviewer_keywords: ["*PDSREG_JOIN_INFO","DSREG_JOIN_INFO","DSREG_JOIN_INFO structure [Network Management]","PDSREG_JOIN_INFO","PDSREG_JOIN_INFO structure pointer [Network Management]","lmjoin/DSREG_JOIN_INFO","lmjoin/PDSREG_JOIN_INFO","netmgmt.dsreg_join_info"]
old-location: netmgmt\dsreg_join_info.htm
tech.root: NetMgmt
ms.assetid: 9B0F7BE3-BDCD-437E-9157-9A646A2A20E2
ms.date: 12/05/2018
ms.keywords: '*PDSREG_JOIN_INFO, DSREG_JOIN_INFO, DSREG_JOIN_INFO structure [Network Management], PDSREG_JOIN_INFO, PDSREG_JOIN_INFO structure pointer [Network Management], lmjoin/DSREG_JOIN_INFO, lmjoin/PDSREG_JOIN_INFO, netmgmt.dsreg_join_info'
req.header: lmjoin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: DSREG_JOIN_INFO, *PDSREG_JOIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSREG_JOIN_INFO
 - lmjoin/_DSREG_JOIN_INFO
 - PDSREG_JOIN_INFO
 - lmjoin/PDSREG_JOIN_INFO
 - DSREG_JOIN_INFO
 - lmjoin/DSREG_JOIN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - lmjoin.h
api_name:
 - DSREG_JOIN_INFO
---

## -description

Contains information about how a device is joined to Microsoft Azure Active Directory.

## -struct-fields

### -field joinType

An enumeration value that specifies the type of the join.

### -field pJoinCertificate

Representations of the certification for the join.

### -field pszDeviceId

The identifier of the device.

### -field pszIdpDomain

A string that represents Azure Active Directory (Azure AD).

### -field pszTenantId

The identifier of the joined Azure AD tenant.

### -field pszJoinUserEmail

The email address for the joined account.

### -field pszTenantDisplayName

The display name for the joined account.

### -field pszMdmEnrollmentUrl

The URL to use to enroll in the Mobile Device Management (MDM) service.

### -field pszMdmTermsOfUseUrl

The URL that provides information about the terms of use for the MDM service.

### -field pszMdmComplianceUrl

The URL that provides information about compliance for the MDM service.

### -field pszUserSettingSyncUrl

The URL for synchronizing user settings.

### -field pUserInfo

Information about the user account  that was used to join a device to Azure AD.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>

<a href="/windows/desktop/api/lmjoin/ne-lmjoin-dsreg_join_type">DSREG_JOIN_TYPE</a>

<a href="/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_user_info">DSREG_USER_INFO</a>
