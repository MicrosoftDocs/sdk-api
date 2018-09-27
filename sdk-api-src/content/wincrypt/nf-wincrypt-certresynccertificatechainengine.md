---
UID: NF:wincrypt.CertResyncCertificateChainEngine
title: CertResyncCertificateChainEngine function
author: windows-sdk-content
description: Resyncs the certificate chain engine, which resynchronizes the stores the store's engine and updates the engine caches.
old-location: security\certresynccertificatechainengine.htm
tech.root: seccrypto
ms.assetid: D8674AD1-0407-4D1E-9E21-60CAC6D01FC5
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CertResyncCertificateChainEngine, CertResyncCertificateChainEngine function [Security], security.certresynccertificatechainengine, wincrypt/CertResyncCertificateChainEngine
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - crypt32.dll
api_name:
 - CertResyncCertificateChainEngine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertResyncCertificateChainEngine function


## -description


Resyncs the certificate chain engine, which resynchronizes the stores the store's engine and updates the engine caches.


## -parameters




### -param hChainEngine [in, optional]

The chain engine to resynchronize.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



