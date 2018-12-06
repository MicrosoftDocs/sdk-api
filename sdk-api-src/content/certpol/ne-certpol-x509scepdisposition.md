---
UID: NE:certpol.X509SCEPDisposition
title: X509SCEPDisposition
author: windows-sdk-content
description: Describes the resulting disposition of a request to process a response message.
old-location: security\x509scepdisposition.htm
tech.root: seccertenroll
ms.assetid: 635AAD37-261F-4F38-AD00-B3E8A5C55ABF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SCEPDispositionFailure, SCEPDispositionPending, SCEPDispositionSuccess, X509SCEPDisposition, X509SCEPDisposition enumeration [Security], certpol/SCEPDispositionFailure, certpol/SCEPDispositionPending, certpol/SCEPDispositionSuccess, certpol/X509SCEPDisposition, security.x509scepdisposition
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - certpol.h
api_name:
 - X509SCEPDisposition
product: Windows
targetos: Windows
req.typenames: X509SCEPDisposition
req.redist: 
---

# X509SCEPDisposition enumeration


## -description


The <b>X509SCEPDisposition</b> enumeration   describes the resulting disposition of a request to process a response message. This enumeration is used by the <a href="https://msdn.microsoft.com/fcbac911-9e37-4994-bbb6-544b19a92749">IX509SCEPEnrollment</a> interface.


## -enum-fields




### -field SCEPDispositionUnknown


### -field SCEPDispositionSuccess

The request was successful.


### -field SCEPDispositionFailure

The request failed.


### -field SCEPDispositionPending

The request has not completed yet.


### -field SCEPDispositionPendingChallenge




## -see-also




<a href="https://msdn.microsoft.com/4254fdf3-473f-4f22-a08f-13481fd9f779">ProcessResponseMessage</a>
 

 

