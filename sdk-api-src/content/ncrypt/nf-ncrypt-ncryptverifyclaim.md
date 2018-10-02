---
UID: NF:ncrypt.NCryptVerifyClaim
title: NCryptVerifyClaim function
author: windows-sdk-content
description: Verifies a key attestation claim.
old-location: security\ncryptverifyclaim.htm
tech.root: SecCNG
ms.assetid: D3C837A5-49D7-4099-B8FE-37364A275A73
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NCryptVerifyClaim, NCryptVerifyClaim function [Security], ncrypt/NCryptVerifyClaim, security.ncryptverifyclaim
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ncrypt.dll
api_name:
 - NCryptVerifyClaim
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptVerifyClaim function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Verifies a key attestation claim.


## -parameters




### -param hSubjectKey [in]

The subject key handle for the claim.


### -param hAuthorityKey [in, optional]

The authority key handle to use when verifying the claim. This parameter is optional because the authority key is self-contained for certain claim types.


### -param dwClaimType [in]

The type of claim.


### -param pParameterList [in, optional]

An optional parameter list.


### -param pbClaimBlob [in]

The input claim blob.


### -param cbClaimBlob [in]


### -param pOutput [out]

The output blob.


### -param dwFlags [in]

As of Windows 10, no  flags are defined. This parameter should be set to 0.


## -returns



Returns a status code that indicates the success or failure of the function.



