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

# _CERT_POLICY_CONSTRAINTS_INFO structure


## -description


The <b>CERT_POLICY_CONSTRAINTS_INFO</b> structure contains established policies for accepting certificates as trusted.


## -struct-fields




### -field fRequireExplicitPolicy

<b>BOOL</b> flag indicating whether explicit policy information is required.


### -field dwRequireExplicitPolicySkipCerts

<b>DWORD</b> indicating the number of required explicit policy certificates.


### -field fInhibitPolicyMapping

<b>BOOL</b> flag indicating whether policy mapping is inhibited.


### -field dwInhibitPolicyMappingSkipCerts

<b>DWORD</b> indicating the number of policy mapping certificates to be skipped.

