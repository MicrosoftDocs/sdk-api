---
UID: NS:wincrypt._CERT_REVOCATION_CRL_INFO
title: "_CERT_REVOCATION_CRL_INFO"
author: windows-sdk-content
description: Contains information updated by a certificate revocation list (CRL) revocation type handler.
old-location: security\cert_revocation_crl_info.htm
tech.root: seccrypto
ms.assetid: 069ff521-90fd-4de8-9b5c-045e44e87f75
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCERT_REVOCATION_CRL_INFO, CERT_REVOCATION_CRL_INFO, CERT_REVOCATION_CRL_INFO structure [Security], PCERT_REVOCATION_CRL_INFO, PCERT_REVOCATION_CRL_INFO structure pointer [Security], _CERT_REVOCATION_CRL_INFO, _crypto2_cert_revocation_crl_info, security.cert_revocation_crl_info, wincrypt/CERT_REVOCATION_CRL_INFO, wincrypt/PCERT_REVOCATION_CRL_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_REVOCATION_CRL_INFO
product: Windows
targetos: Windows
req.typenames: CERT_REVOCATION_CRL_INFO, *PCERT_REVOCATION_CRL_INFO
req.redist: 
---

# _CERT_REVOCATION_CRL_INFO structure


## -description


Contains information updated by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) revocation type handler. The <b>CERT_REVOCATION_CRL_INFO</b> structure is used with both base and delta CRLs.


## -struct-fields




### -field cbSize

Size, in bytes, of the structure.


### -field pBaseCrlContext

 


### -field pDeltaCrlContext

 


### -field pCrlEntry

A pointer to an entry in either the base CRL or the delta CRL.


### -field fDeltaCrlEntry

<b>TRUE</b> if <b>pCrlEntry</b> points to an entry in the delta CRL. <b>FALSE</b> if <b>pCrlEntry</b> points to an entry in the base CRL.


#### - pBaseCRLContext

A pointer to a base CRL context.


#### - pDeltaCRLContext

A pointer to a delta CRL context.

