---
UID: NF:sspi.SspiCopyAuthIdentity
title: SspiCopyAuthIdentity function
author: windows-driver-content
description: Creates a copy of the specified opaque credential structure.
old-location: security\sspicopyauthidentity.htm
old-project: SecAuthN
ms.assetid: e53807bf-b5a1-4479-a73b-dd85c5da173e
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: SspiCopyAuthIdentity, SspiCopyAuthIdentity function [Security], security.sspicopyauthidentity, sspi/SspiCopyAuthIdentity
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
-	SspiCopyAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SspiCopyAuthIdentity function


## -description


Creates a copy of the specified opaque credential structure.


## -parameters




### -param AuthData [in]

The credential structure to be copied.


### -param AuthDataCopy [out]

The structure that receives the copy of the structure specified by the <i>AuthData</i> parameter.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



