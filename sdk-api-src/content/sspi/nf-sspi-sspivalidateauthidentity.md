---
UID: NF:sspi.SspiValidateAuthIdentity
title: SspiValidateAuthIdentity function
author: windows-sdk-content
description: Indicates whether the specified identity structure is valid.
old-location: security\sspivalidateauthidentity.htm
old-project: SecAuthN
ms.assetid: 82733abd-d984-4902-b6e4-c3809171ad51
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SspiValidateAuthIdentity, SspiValidateAuthIdentity function [Security], security.sspivalidateauthidentity, sspi/SspiValidateAuthIdentity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sspi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
api_name:
 - SspiValidateAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiValidateAuthIdentity function


## -description


Indicates whether the specified identity structure is valid.


## -parameters




### -param AuthData [in]

The identity structure to test.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>, which indicates that the identity structure specified by the <i>AuthData</i> parameter is valid.

If the function fails, it returns a nonzero error code that indicates that the identity structure specified by the <i>AuthData</i> parameter is not valid.



