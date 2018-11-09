---
UID: NS:schannel._SecPkgContext_IssuerListInfoEx
title: "_SecPkgContext_IssuerListInfoEx"
author: windows-sdk-content
description: The SecPkgContext_IssuerListInfoEx structure holds a list of trusted certification authorities (CAs).
old-location: security\secpkgcontext_issuerlistinfoex.htm
tech.root: secauthn
ms.assetid: cf1ccd40-36bf-4597-b34f-d26cef63d800
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PSecPkgContext_IssuerListInfoEx, PSecPkgContext_IssuerListInfoEx, PSecPkgContext_IssuerListInfoEx structure pointer [Security], SecPkgContext_IssuerListInfoEx, SecPkgContext_IssuerListInfoEx structure [Security], _SecPkgContext_IssuerListInfoEx, _ssp_secpkgcontext_issuerlistinfoex, schannel/PSecPkgContext_IssuerListInfoEx, schannel/SecPkgContext_IssuerListInfoEx, security.secpkgcontext_issuerlistinfoex"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: schannel.h
req.include-header: Schnlsp.h
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
 - Schannel.h
api_name:
 - SecPkgContext_IssuerListInfoEx
product: Windows
targetos: Windows
req.typenames: SecPkgContext_IssuerListInfoEx, *PSecPkgContext_IssuerListInfoEx
req.redist: 
---

# _SecPkgContext_IssuerListInfoEx structure


## -description


The <b>SecPkgContext_IssuerListInfoEx</b> structure holds a list of trusted <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> (CAs). This structure is used by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function.

This attribute is supported only by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).

This attribute is available only to client applications and can be queried only after a call to the <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function returns the value <b>SEC_E_INCOMPLETE_CREDENTIALS</b>.


## -struct-fields




### -field aIssuers

A pointer to 
an array of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structures that contains a list of the names of CAs that the server trusts.

When you have finished using the data in this array, free it by calling the <a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


### -field cIssuers

The number of names in <b>aIssuers</b>.

