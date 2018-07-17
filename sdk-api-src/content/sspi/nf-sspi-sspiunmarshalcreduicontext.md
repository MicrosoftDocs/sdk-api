---
UID: NF:sspi.SspiUnmarshalCredUIContext
title: SspiUnmarshalCredUIContext function
author: windows-sdk-content
description: Deserializes credential information obtained by a credential provider during a previous call to the ICredentialProvider::SetSerialization method.
old-location: security\sspiunmarshalcreduicontext.htm
old-project: secauthn
ms.assetid: c8861b27-d42d-4f7f-96c7-718f23fbaf86
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: SspiUnmarshalCredUIContext, SspiUnmarshalCredUIContext function [Security], security.sspiunmarshalcreduicontext, sspi/SspiUnmarshalCredUIContext
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
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - SspiUnmarshalCredUIContext
product: Windows
targetos: Windows
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SspiUnmarshalCredUIContext function


## -description


Deserializes credential information obtained by a credential provider during  a previous call to the <a href="https://msdn.microsoft.com/library/Bb776043(v=VS.85).aspx">ICredentialProvider::SetSerialization</a> method.


## -parameters




### -param MarshaledCredUIContext [in]

The serialized credential information obtained as the <b>rgbSerialization</b> member of the <a href="https://msdn.microsoft.com/library/Bb773242(v=VS.85).aspx">CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</a> structure retrieved from a call to the <a href="https://msdn.microsoft.com/library/Bb776043(v=VS.85).aspx">ICredentialProvider::SetSerialization</a> method.


### -param MarshaledCredUIContextLength [in]

The size, in bytes, of the <i>MarshaledCredUIContext</i> buffer.


### -param CredUIContext [out]

A pointer to a <a href="https://msdn.microsoft.com/ac9410eb-ec1b-494c-8e8b-6d161ff2b41c">SEC_WINNT_CREDUI_CONTEXT</a> structure that specifies the deserialized credential information.


## -returns




                  If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



