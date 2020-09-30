---
UID: NF:certpoleng.PstGetCertificates
title: PstGetCertificates function (certpoleng.h)
description: Retrieves certificate chains that specify certificates that can be used to authenticate a user on the specified server.
helpviewer_keywords: ["PstGetCertificates","PstGetCertificates function [Security]","certpoleng/PstGetCertificates","security.pstgetcertificates"]
old-location: security\pstgetcertificates.htm
tech.root: security
ms.assetid: 3dfe3a7b-aefd-487a-a826-065e80f21eb5
ms.date: 12/05/2018
ms.keywords: PstGetCertificates, PstGetCertificates function [Security], certpoleng/PstGetCertificates, security.pstgetcertificates
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PstGetCertificates
 - certpoleng/PstGetCertificates
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Certpoleng.dll
api_name:
 - PstGetCertificates
---

# PstGetCertificates function


## -description

Retrieves certificate chains that specify certificates that can be used to authenticate a user on the specified server.

## -parameters

### -param pTargetName [in]

The name of the server to check.

### -param cCriteria [in]

The number of elements in the <i>rgpCriteria</i> array.

### -param rgpCriteria [in, optional]

A constant pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_select_criteria">CERT_SELECT_CRITERIA</a> structures that specify the criteria used to select certificate chains.

### -param bIsClient [in]

<b>TRUE</b> if the caller is the client; otherwise, <b>FALSE</b>.

### -param pdwCertChainContextCount [out]

The number of elements in the <i>ppCertChainContexts</i> array.

### -param ppCertChainContexts [out]

The address of a pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structures that specifies the certificate chains of certificates that can be used to authenticate a user on the server specified by the <i>pTargetName</i> parameter.

## -returns

If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.