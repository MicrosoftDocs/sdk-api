---
UID: NF:certpoleng.PstGetUserNameForCertificate
title: PstGetUserNameForCertificate function (certpoleng.h)
description: Retrieves the user name associated with the specified certificate.
helpviewer_keywords: ["PstGetUserNameForCertificate","PstGetUserNameForCertificate function [Security]","certpoleng/PstGetUserNameForCertificate","security.pstgetusernameforcertificate"]
old-location: security\pstgetusernameforcertificate.htm
tech.root: security
ms.assetid: abef13bc-0d63-4c71-a1cb-9ade26b41da3
ms.date: 12/05/2018
ms.keywords: PstGetUserNameForCertificate, PstGetUserNameForCertificate function [Security], certpoleng/PstGetUserNameForCertificate, security.pstgetusernameforcertificate
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
 - PstGetUserNameForCertificate
 - certpoleng/PstGetUserNameForCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-certpoleng-l1-1-0.dll
 - Certpoleng.dll
api_name:
 - PstGetUserNameForCertificate
---

# PstGetUserNameForCertificate function


## -description

Retrieves the user name associated with the specified certificate.

## -parameters

### -param pCertContext [in]

A constant pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that specifies the certificate for which to obtain the user name.

### -param UserName [out]

The user name associated with the certificate specified by the <i>pCertContext</i> parameter.

## -returns

If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.