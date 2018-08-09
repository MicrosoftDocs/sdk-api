---
UID: NF:sspi.SspiUnmarshalAuthIdentity
title: SspiUnmarshalAuthIdentity function
author: windows-sdk-content
description: Deserializes the specified array of byte values into an identity structure.
old-location: security\sspiunmarshalauthidentity.htm
old-project: secauthn
ms.assetid: 89798b37-808a-4174-8362-a2dc4ee1b460
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SspiUnmarshalAuthIdentity, SspiUnmarshalAuthIdentity function [Security], security.sspiunmarshalauthidentity, sspi/SspiUnmarshalAuthIdentity
ms.prod: windows
ms.technology: windows-sdk
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
 - SspiUnmarshalAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiUnmarshalAuthIdentity function


## -description


Deserializes the specified array of byte values into an identity structure.


## -parameters




### -param AuthIdentityLength [in]

The size, in bytes, of the <i>AuthIdentityByteArray</i> array.


### -param AuthIdentityByteArray [in]

The array of byte values to deserialize.


### -param ppAuthIdentity [out]

The deserialized identity structure.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



