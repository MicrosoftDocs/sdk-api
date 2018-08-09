---
UID: NE:certpol.X509SCEPFailInfo
title: X509SCEPFailInfo
author: windows-sdk-content
description: Describes the nature of an SCEP certificate enrollment failure.
old-location: security\x509scepfailinfo.htm
old-project: seccertenroll
ms.assetid: A2C314FB-A348-41CE-9736-2BDE05F7E70E
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: SCEPFailBadAlgorithm, SCEPFailBadCertId, SCEPFailBadMessageCheck, SCEPFailBadRequest, SCEPFailBadTime, X509SCEPFailInfo, X509SCEPFailInfo enumeration [Security], certpol/SCEPFailBadAlgorithm, certpol/SCEPFailBadCertId, certpol/SCEPFailBadMessageCheck, certpol/SCEPFailBadRequest, certpol/SCEPFailBadTime, certpol/X509SCEPFailInfo, security.x509scepfailinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certpol.h
req.include-header: CertEnroll.h
req.target-type: Windows
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
tech.root: 
req.typenames: X509SCEPFailInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - certpol.h
api_name:
 - X509SCEPFailInfo
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: 
req.irql: 
---

# X509SCEPFailInfo enumeration


## -description


The <b>X509SCEPFailInfo</b> enumeration   describes the nature of an SCEP certificate enrollment failure. This enumeration is used by the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface.


## -enum-fields




### -field SCEPFailUnknown


### -field SCEPFailBadAlgorithm

Failure due to an unrecognized or unsupported algorithm.


### -field SCEPFailBadMessageCheck

The integrity check failed.


### -field SCEPFailBadRequest

The transaction was not permitted or was not supported.


### -field SCEPFailBadTime

The signing time attribute from the PKCS7 authenticated attributes was not sufficiently close to the system time.


### -field SCEPFailBadCertId

No certificate could be identified.


## -see-also




<a href="https://msdn.microsoft.com/4fd76b7e-8b19-46da-b352-7668917a6585">FailInfo</a>
 

 

