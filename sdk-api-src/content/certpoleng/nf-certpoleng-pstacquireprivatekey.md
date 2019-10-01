---
UID: NF:certpoleng.PstAcquirePrivateKey
title: PstAcquirePrivateKey function (certpoleng.h)
author: windows-sdk-content
description: Associates the caller's private key with the specified certificate.
old-location: security\pstacquireprivatekey.htm
tech.root: SecAuthN
ms.assetid: dad2886b-5a74-433f-bd58-deb130104e33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PstAcquirePrivateKey, PstAcquirePrivateKey function [Security], certpoleng/PstAcquirePrivateKey, security.pstacquireprivatekey
ms.topic: function
f1_keywords: 
 - "certpoleng/PstAcquirePrivateKey"
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
 - PstAcquirePrivateKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PstAcquirePrivateKey function


## -description


Associates the caller's <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> with the specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>.


## -parameters




### -param pCert [in]

The certificate with which to associate the private key.


## -returns



If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



