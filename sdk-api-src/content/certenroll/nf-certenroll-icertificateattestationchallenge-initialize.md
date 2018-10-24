---
UID: NF:certenroll.ICertificateAttestationChallenge.Initialize
title: ICertificateAttestationChallenge::Initialize
author: windows-sdk-content
description: Initialize using the full Certificate Management over CMS (CMC) response returned from the CA.
old-location: security\icertificateattestationchallenge_initialize.htm
tech.root: SecCertEnroll
ms.assetid: d4dbda92-4523-4adb-9b88-b2bc763570fd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICertificateAttestationChallenge interface [Security],Initialize method, ICertificateAttestationChallenge.Initialize, ICertificateAttestationChallenge::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertificateAttestationChallenge interface, certenroll/ICertificateAttestationChallenge::Initialize, security.icertificateattestationchallenge_initialize
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
 - ICertificateAttestationChallenge.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificateAttestationChallenge::Initialize


## -description


Initialize using the full <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) response returned from the CA.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/b42628ae-deed-497b-a20f-d175843b79c2">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  response. The default value is XCN_CRYPT_STRING_BASE64.


### -param strPendingFullCmcResponseWithChallenge [in]

The pending CMC response from the CA.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CA should have returned a pending CMC response. The content of the CMC response should contain a challenge. There must be only one CMC response and it must contain pending information.




## -see-also




<a href="https://msdn.microsoft.com/3b8d3104-5824-4801-9b74-59307e650662">ICertificateAttestationChallenge</a>
 

 

