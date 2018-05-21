---
UID: NF:sspi.SspiZeroAuthIdentity
title: SspiZeroAuthIdentity function
author: windows-driver-content
description: Fills the block of memory associated with the specified identity structure with zeros.
old-location: security\sspizeroauthidentity.htm
old-project: SecAuthN
ms.assetid: 50b1f24a-c802-4691-a450-316cb31bf44d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: SspiZeroAuthIdentity, SspiZeroAuthIdentity function [Security], security.sspizeroauthidentity, sspi/SspiZeroAuthIdentity
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
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	SspiCli.dll
api_name:
-	SspiZeroAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiZeroAuthIdentity function


## -description


Fills the block of memory associated with the specified identity structure with zeros.


## -parameters




### -param AuthData [in]

The identity structure to fill with zeros.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



