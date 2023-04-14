---
UID: NF:sspi.SspiUnmarshalAuthIdentity
title: SspiUnmarshalAuthIdentity function (sspi.h)
description: Deserializes the specified array of byte values into an identity structure.
helpviewer_keywords: ["SspiUnmarshalAuthIdentity","SspiUnmarshalAuthIdentity function [Security]","security.sspiunmarshalauthidentity","sspi/SspiUnmarshalAuthIdentity"]
old-location: security\sspiunmarshalauthidentity.htm
tech.root: security
ms.assetid: 89798b37-808a-4174-8362-a2dc4ee1b460
ms.date: 12/05/2018
ms.keywords: SspiUnmarshalAuthIdentity, SspiUnmarshalAuthIdentity function [Security], security.sspiunmarshalauthidentity, sspi/SspiUnmarshalAuthIdentity
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiUnmarshalAuthIdentity
 - sspi/SspiUnmarshalAuthIdentity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - SspiCli.dll
 - secur32.dll
api_name:
 - SspiUnmarshalAuthIdentity
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

