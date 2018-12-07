---
UID: NF:sspi.SspiFreeAuthIdentity
title: SspiFreeAuthIdentity function
author: windows-sdk-content
description: Frees the memory allocated for the specified identity structure.
old-location: security\sspifreeauthidentity.htm
tech.root: secauthn
ms.assetid: 6199f66e-7adb-4bb9-8e77-a735e31dd5f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SspiFreeAuthIdentity, SspiFreeAuthIdentity function [Security], security.sspifreeauthidentity, sspi/SspiFreeAuthIdentity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
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
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiFreeAuthIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SspiFreeAuthIdentity function


## -description


Frees the memory allocated for the specified identity structure.


## -parameters




### -param AuthData [in]

The identity structure to free.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



