---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DSREG_JOIN_INFO structure


## -description


Contains information about how a device is joined to Microsoft Azure Active Directory.


## -struct-fields




### -field joinType

An enumeration value that specifies the type of the join. 


### -field pJoinCertificate

Representations of the certification for the join.


### -field pszDeviceId

 


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


#### - pszDeviceID

The identifier of the device.


## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/E29BCBE0-222F-4CA8-97BC-6FE1B6F97A67">DSREG_JOIN_TYPE</a>



<a href="https://msdn.microsoft.com/5E639988-0F53-40D7-BBEC-F78B3D124CC0">DSREG_USER_INFO</a>
 

 

