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

