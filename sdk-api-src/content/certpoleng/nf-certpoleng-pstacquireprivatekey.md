---
UID: NF:certpoleng.PstAcquirePrivateKey
title: PstAcquirePrivateKey function
author: windows-sdk-content
description: Associates the caller's private key with the specified certificate.
old-location: security\pstacquireprivatekey.htm
tech.root: secauthn
ms.assetid: dad2886b-5a74-433f-bd58-deb130104e33
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: PstAcquirePrivateKey, PstAcquirePrivateKey function [Security], certpoleng/PstAcquirePrivateKey, security.pstacquireprivatekey
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
 - PstAcquirePrivateKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PstAcquirePrivateKey function


## -description


Associates the caller's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> with the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>.


## -parameters




### -param pCert [in]

The certificate with which to associate the private key.


## -returns



If the function succeeds, return <b>STATUS_SUCCESS</b>.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.



