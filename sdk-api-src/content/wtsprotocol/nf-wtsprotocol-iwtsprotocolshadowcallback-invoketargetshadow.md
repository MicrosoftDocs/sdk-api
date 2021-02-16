---
UID: NF:wtsprotocol.IWTSProtocolShadowCallback.InvokeTargetShadow
title: IWTSProtocolShadowCallback::InvokeTargetShadow (wtsprotocol.h)
description: IWTSProtocolShadowCallback::InvokeTargetShadow is no longer available. Instead, use IWRdsProtocolShadowCallback::InvokeTargetShadow.
helpviewer_keywords: ["IWTSProtocolShadowCallback interface [Remote Desktop Services]","InvokeTargetShadow method","IWTSProtocolShadowCallback.InvokeTargetShadow","IWTSProtocolShadowCallback::InvokeTargetShadow","InvokeTargetShadow","InvokeTargetShadow method [Remote Desktop Services]","InvokeTargetShadow method [Remote Desktop Services]","IWTSProtocolShadowCallback interface","termserv.iwtsprotocolshadowcallback_invoketargetshadow","wtsprotocol/IWTSProtocolShadowCallback::InvokeTargetShadow"]
old-location: termserv\iwtsprotocolshadowcallback_invoketargetshadow.htm
tech.root: TermServ
ms.assetid: 1ce090cd-6824-4a89-acb4-138a1d0f6f76
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowCallback interface [Remote Desktop Services],InvokeTargetShadow method, IWTSProtocolShadowCallback.InvokeTargetShadow, IWTSProtocolShadowCallback::InvokeTargetShadow, InvokeTargetShadow, InvokeTargetShadow method [Remote Desktop Services], InvokeTargetShadow method [Remote Desktop Services],IWTSProtocolShadowCallback interface, termserv.iwtsprotocolshadowcallback_invoketargetshadow, wtsprotocol/IWTSProtocolShadowCallback::InvokeTargetShadow
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolShadowCallback::InvokeTargetShadow
 - wtsprotocol/IWTSProtocolShadowCallback::InvokeTargetShadow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolShadowCallback.InvokeTargetShadow
---

# IWTSProtocolShadowCallback::InvokeTargetShadow


## -description

<p class="CCE_Message">[<b>IWTSProtocolShadowCallback::InvokeTargetShadow</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowcallback-invoketargetshadow">IWRdsProtocolShadowCallback::InvokeTargetShadow</a>.]

Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

## -parameters

### -param pTargetServerName [in]

A pointer to a string that contains the name of the shadow target server.

### -param TargetSessionId [in]

An integer that specifies the ID of the target session to shadow.

### -param pParam1 [in]

A pointer to a byte that contains an arbitrary parameter.

### -param Param1Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam1</i> parameter.

### -param pParam2 [in]

A pointer to a byte that contains an arbitrary parameter.

### -param Param2Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam2</i> parameter.

### -param pParam3 [in]

A pointer to a byte that contains an arbitrary parameter.

### -param Param3Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam3</i> parameter.

### -param pParam4 [in]

A pointer to a byte that contains an arbitrary parameter.

### -param Param4Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam4</i> parameter.

### -param pClientName [in]

A pointer to a string that contains the name of the shadow client.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The four parameters <i>pParam1</i>, <i>pParam2</i>, <i>pParam3</i>, and <i>pParam4</i> can contain any information that must be exchanged between the shadow client and the shadow target. The Remote Desktop Services service passes the information without modification.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback">IWTSProtocolShadowCallback</a>