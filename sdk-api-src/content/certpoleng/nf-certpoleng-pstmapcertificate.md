---
UID: NF:certpoleng.PstMapCertificate
title: PstMapCertificate function
author: windows-sdk-content
description: Retrieves a structure that specifies information that can be used to create a user token associated with the specified certificate.
old-location: security\pstmapcertificate.htm
tech.root: secauthn
ms.assetid: b4e7e3b0-97ec-4c59-b2a1-cb83a27df94d
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: PstMapCertificate, PstMapCertificate function [Security], certpoleng/PstMapCertificate, security.pstmapcertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: certpoleng.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certpoleng.lib
req.dll: Certpoleng.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certpoleng.dll
api_name:
 - PstMapCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PstMapCertificate function


## -description


Retrieves a structure that specifies information that can be used to create a user token associated with the specified certificate.


## -parameters




### -param pCert [in]

A constant pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that specifies the certificate for which to obtain token information.


### -param pTokenInformationType [out]

A pointer to a value of the <a href="https://msdn.microsoft.com/c8bf5b8d-6cb1-469d-a451-6cceafda24cf">LSA_TOKEN_INFORMATION_TYPE</a> enumeration that indicates the type of structure pointed to by the <i>ppTokenInformation</i> parameter.


### -param ppTokenInformation [out]

The address of a pointer to a structure that specifies information that can be used to create a user token.


## -returns



If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



