---
UID: NF:sspi.SspiUnmarshalCredUIContext
title: SspiUnmarshalCredUIContext function (sspi.h)
description: Deserializes credential information obtained by a credential provider during a previous call to the ICredentialProvider::SetSerialization method.
helpviewer_keywords: ["SspiUnmarshalCredUIContext","SspiUnmarshalCredUIContext function [Security]","security.sspiunmarshalcreduicontext","sspi/SspiUnmarshalCredUIContext"]
old-location: security\sspiunmarshalcreduicontext.htm
tech.root: security
ms.assetid: c8861b27-d42d-4f7f-96c7-718f23fbaf86
ms.date: 12/05/2018
ms.keywords: SspiUnmarshalCredUIContext, SspiUnmarshalCredUIContext function [Security], security.sspiunmarshalcreduicontext, sspi/SspiUnmarshalCredUIContext
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
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiUnmarshalCredUIContext
 - sspi/SspiUnmarshalCredUIContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - SspiUnmarshalCredUIContext
---

# SspiUnmarshalCredUIContext function


## -description

Deserializes credential information obtained by a credential provider during  a previous call to the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">ICredentialProvider::SetSerialization</a> method.

## -parameters

### -param MarshaledCredUIContext [in]

The serialized credential information obtained as the <b>rgbSerialization</b> member of the <a href="/windows/win32/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure retrieved from a call to the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovider-setserialization">ICredentialProvider::SetSerialization</a> method.

### -param MarshaledCredUIContextLength [in]

The size, in bytes, of the <i>MarshaledCredUIContext</i> buffer.

### -param CredUIContext [out]

A pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_credui_context">SEC_WINNT_CREDUI_CONTEXT</a> structure that specifies the deserialized credential information.

## -returns

If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.