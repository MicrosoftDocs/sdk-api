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

# IKEEXT_CERT_CRITERIA_NAME_TYPE_ enumeration


## -description


The <b>IKEEXT_CERT_CRITERIA_NAME_TYPE</b> enumerated type specifies the type of NAME fields possible for a certificate selection "subject" criteria.


## -enum-fields




### -field IKEEXT_CERT_CRITERIA_DNS

DNS name in the Subject Alternative Name of the certificate.


### -field IKEEXT_CERT_CRITERIA_UPN

UPN name in the Subject Alternative Name of the certificate.


### -field IKEEXT_CERT_CRITERIA_RFC822

RFC 822 name in the Subject Alternative Name of the certificate.


### -field IKEEXT_CERT_CRITERIA_CN

CN in the Subject of the certificate.


### -field IKEEXT_CERT_CRITERIA_OU

OU in the Subject of the certificate.


### -field IKEEXT_CERT_CRITERIA_O

O in the Subject of the certificate.


### -field IKEEXT_CERT_CRITERIA_DC

DC in the Subject of the certificate.


### -field IKEEXT_CERT_CRITERIA_NAME_TYPE_MAX

Maximum value for testing purposes.

