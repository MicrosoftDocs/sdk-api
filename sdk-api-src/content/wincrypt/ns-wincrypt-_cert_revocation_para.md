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

# _CERT_REVOCATION_PARA structure


## -description


The <b>CERT_REVOCATION_PARA</b> structure is passed in calls to 
the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function to assist in finding the issuer of the context to be verified. The <b>CERT_REVOCATION_PARA</b> structure is an optional parameter in the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pIssuerCert

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the certificate of the issuer of a certificate specified in the <i>rgpvContext</i> array in the 
<a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> parameter list.


### -field cCertStore

When set, contains the number of elements in the <b>rgCertStore</b> array. Set to zero if you are not supplying  a list of store handles in the <i>rgCertStore</i> parameter.


### -field rgCertStore

An array of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> handles. Specifies a set of stores that are searched for issuer certificates.  If <i>rgCertStore</i> is not set, the default stores are searched.


### -field hCrlStore

Optional store handle. When specified, a handler that uses <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) can search this store for CRLs.


### -field pftTimeToUse

A pointer to a <b>FILETIME</b> version of UTC time. When specified, the handler must, if possible, determine revocation status relative to the time given. If <b>NULL</b> or the handler cannot determine the status relative to the <b>pftTimeToUse</b> value, revocation status can be determined independent of time or relative to current time.


### -field dwUrlRetrievalTimeout

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. The time-out, in milliseconds, that the revocation handler will wait when attempting to retrieve revocation information. If it is set to zero, the revocation handler's default time-out is used. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to zero if it is unused.


### -field fCheckFreshnessTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. If <b>TRUE</b>, an attempt is made to retrieve a new CRL if the issue date of the CRL is less than or equal to the Current Time minus <b>dwFreshnessTime</b>. If this flag is not set, the CRL's NextUpdate time is used. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to <b>FALSE</b> if it is unused. 


### -field dwFreshnessTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. The time, in seconds, is used to determine whether an attempt will be made to retrieve a new CRL. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to zero if it is unused. 


### -field pftCurrentTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. A pointer to a <b>FILETIME</b> structure that is used in the freshness time check. If the value of this pointer is null, the revocation handler uses the current time. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused. 


### -field pCrlInfo

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined.  This member contains a pointer to a PCERT_REVOCATION_CRL_INFO structure that contains CRL context information. The CRL information is only applicable to the last <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> checked. To access the information in this CRL, call the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function with <i>cContext</i> set to 1. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, the member must be set to null if it is unused.


### -field pftCacheResync

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. This member contains a pointer to a <b>FILETIME</b> structure that specifies the use of cached information. Any information cached  before the specified time is considered invalid and new information is retrieved. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused.

<b>Windows Server 2003 and Windows XP:  </b>This member is not used.


### -field pChainPara

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. This member contains a pointer to a <a href="https://msdn.microsoft.com/9cdcc81a-aef1-4a1e-94f8-7aa461225dae">CERT_REVOCATION_CHAIN_PARA</a> structure that contains parameters used for building a chain for an independent OCSP signer certificate. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not used in the listed systems. The member is available beginning with Windows Vista with SP1.


## -remarks



The <b>CERT_REVOCATION_PARA</b> structure provides additional information that the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function can use to determine the context issuer.

 If your application must check the freshness of the CRL or resynchronize the CRL cache, you can provide extra structure members to assist  the <a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a> function with this.  To include the additional structure members, define the constant <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> in your application before including Wincrypt.h




## -see-also




<a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a>
 

 

