---
UID: NF:certenroll.IX509SCEPEnrollment.put_ServerCapabilities
title: IX509SCEPEnrollment::put_ServerCapabilities
author: windows-sdk-content
description: Sets the preferred hash and encryption algorithms for the request.
old-location: security\ix509scepenrollment_servercapabilities.htm
tech.root: SecCertEnroll
ms.assetid: fcfed23f-7798-4b56-afcd-65975a2d39bd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509SCEPEnrollment interface [Security],ServerCapabilities property, IX509SCEPEnrollment.ServerCapabilities, IX509SCEPEnrollment.put_ServerCapabilities, IX509SCEPEnrollment::ServerCapabilities, IX509SCEPEnrollment::put_ServerCapabilities, ServerCapabilities property [Security], ServerCapabilities property [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::ServerCapabilities, certenroll/IX509SCEPEnrollment::put_ServerCapabilities, put_ServerCapabilities, security.ix509scepenrollment_servercapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.ServerCapabilities
 - IX509SCEPEnrollment.put_ServerCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509SCEPEnrollment.put_ServerCapabilities
: 
---

# IX509SCEPEnrollment::put_ServerCapabilities


## -description


Sets the preferred hash and encryption algorithms for the request.

This property is write-only.


## -parameters


## -remarks



If you do not set this property, then the default hash and encryption algorithms will be used.

This property must be set before calling the <a href="https://msdn.microsoft.com/en-us/library/Dn424976(v=VS.85).aspx">CreateRequestMessage</a>, <a href="https://msdn.microsoft.com/en-us/library/Dn424978(v=VS.85).aspx">CreateRetrievePendingMessage</a>, or <a href="https://msdn.microsoft.com/en-us/library/Dn424977(v=VS.85).aspx">CreateRetrieveCertificateMessage</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

