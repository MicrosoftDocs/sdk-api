---
UID: NF:wincrypt.CertFreeServerOcspResponseContext
title: CertFreeServerOcspResponseContext function
author: windows-sdk-content
description: Decrements the reference count for a CERT_SERVER_OCSP_RESPONSE_CONTEXT structure.
old-location: security\certfreeserverocspresponsecontext.htm
tech.root: seccrypto
ms.assetid: a07fc1e0-6f06-4336-b33c-d4d6a838b609
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertFreeServerOcspResponseContext, CertFreeServerOcspResponseContext function [Security], security.certfreeserverocspresponsecontext, wincrypt/CertFreeServerOcspResponseContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFreeServerOcspResponseContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFreeServerOcspResponseContext function


## -description


The <b>CertFreeServerOcspResponseContext</b> function decrements the reference count for a <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure. If the reference count becomes zero, memory allocated for the structure is released.


## -parameters




### -param pServerOcspResponseContext [in]

A pointer to a <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure that contains a value returned by the <a href="https://msdn.microsoft.com/07476e43-db6b-4119-8d6b-41143b98744e">CertGetServerOcspResponseContext</a> function.


## -returns



This function has no return value.



