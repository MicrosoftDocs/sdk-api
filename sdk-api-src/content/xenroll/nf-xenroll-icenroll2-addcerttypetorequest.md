---
UID: NF:xenroll.ICEnroll2.addCertTypeToRequest
title: ICEnroll2::addCertTypeToRequest
author: windows-sdk-content
description: Adds a certificate template to a request (used to support the enterprise certification authority (CA)). This method was first defined by the ICEnroll2 interface.
old-location: security\icenroll4_addcerttypetorequest.htm
tech.root: seccrypto
ms.assetid: d2c22689-d386-43d1-a42f-f303a034a087
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CEnroll object [Security],addCertTypeToRequest method, ICEnroll2 interface [Security],addCertTypeToRequest method, ICEnroll2.addCertTypeToRequest, ICEnroll2::addCertTypeToRequest, ICEnroll3 interface [Security],addCertTypeToRequest method, ICEnroll3::addCertTypeToRequest, ICEnroll4 interface [Security],addCertTypeToRequest method, ICEnroll4::addCertTypeToRequest, addCertTypeToRequest, addCertTypeToRequest method [Security], addCertTypeToRequest method [Security],CEnroll object, addCertTypeToRequest method [Security],ICEnroll2 interface, addCertTypeToRequest method [Security],ICEnroll3 interface, addCertTypeToRequest method [Security],ICEnroll4 interface, security.icenroll4_addcerttypetorequest, xenroll/ICEnroll2::addCertTypeToRequest, xenroll/ICEnroll3::addCertTypeToRequest, xenroll/ICEnroll4::addCertTypeToRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.addCertTypeToRequest
 - ICEnroll3.addCertTypeToRequest
 - ICEnroll2.addCertTypeToRequest
 - CEnroll.addCertTypeToRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- ICEnroll2.addCertTypeToRequest
: 
---

# ICEnroll2::addCertTypeToRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addCertTypeToRequest</b> method adds a certificate template to a request (used to support the enterprise <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA)). This method was first defined by the <a href="https://msdn.microsoft.com/12c51daf-a72f-43da-9fb7-20ec261b4917">ICEnroll2</a> interface.

The <b>addCertTypeToRequest</b> method is an advanced topic that is associated with the Microsoft Certificate Services enterprise Policy Module. Its use is not recommended for most applications.

The phrase 'certificate type' is synonymous with 'certificate template'.

method


## -parameters




### -param CertType [in]

The certificate template fully qualified name which is being added to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This value is interpreted by the certification authority.


## -returns



<h3>VB</h3>
 The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.




## -remarks



This method can be called multiple times if more than one certificate template is desired for the request.



