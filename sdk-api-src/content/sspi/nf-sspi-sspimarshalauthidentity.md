---
UID: NF:sspi.SspiMarshalAuthIdentity
title: SspiMarshalAuthIdentity function
author: windows-sdk-content
description: Serializes the specified identity structure into a byte array.
old-location: security\sspimarshalauthidentity.htm
old-project: secauthn
ms.assetid: e43135ad-7fcd-4da6-a4e4-c91c41eeb865
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SspiMarshalAuthIdentity, SspiMarshalAuthIdentity function [Security], security.sspimarshalauthidentity, sspi/SspiMarshalAuthIdentity
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
 - SspiMarshalAuthIdentity
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: SspiCli.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiMarshalAuthIdentity function


## -description


Serializes the specified identity structure into a byte array.


## -parameters




### -param AuthIdentity [in]

The identity structure to serialize.


### -param AuthIdentityLength [out]

The length, in bytes, of the <i>AuthIdentityByteArray</i> array.


### -param AuthIdentityByteArray [out]

A pointer to an array of byte values that represents the identity specified by the <i>AuthIdentity</i> parameter.


## -returns



If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



