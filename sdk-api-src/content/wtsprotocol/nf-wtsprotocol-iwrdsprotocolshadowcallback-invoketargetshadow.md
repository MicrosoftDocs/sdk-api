---
UID: NF:wtsprotocol.IWRdsProtocolShadowCallback.InvokeTargetShadow
title: IWRdsProtocolShadowCallback::InvokeTargetShadow (wtsprotocol.h)
description: Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.
helpviewer_keywords: ["IWRdsProtocolShadowCallback interface [Remote Desktop Services]","InvokeTargetShadow method","IWRdsProtocolShadowCallback.InvokeTargetShadow","IWRdsProtocolShadowCallback::InvokeTargetShadow","InvokeTargetShadow","InvokeTargetShadow method [Remote Desktop Services]","InvokeTargetShadow method [Remote Desktop Services]","IWRdsProtocolShadowCallback interface","termserv.iwrdsprotocolshadowcallback_invoketargetshadow","wtsprotocol/IWRdsProtocolShadowCallback::InvokeTargetShadow"]
old-location: termserv\iwrdsprotocolshadowcallback_invoketargetshadow.htm
tech.root: TermServ
ms.assetid: 76682f4c-2651-4f5d-b96d-4d84bae7933c
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowCallback interface [Remote Desktop Services],InvokeTargetShadow method, IWRdsProtocolShadowCallback.InvokeTargetShadow, IWRdsProtocolShadowCallback::InvokeTargetShadow, InvokeTargetShadow, InvokeTargetShadow method [Remote Desktop Services], InvokeTargetShadow method [Remote Desktop Services],IWRdsProtocolShadowCallback interface, termserv.iwrdsprotocolshadowcallback_invoketargetshadow, wtsprotocol/IWRdsProtocolShadowCallback::InvokeTargetShadow
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolShadowCallback::InvokeTargetShadow
 - wtsprotocol/IWRdsProtocolShadowCallback::InvokeTargetShadow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolShadowCallback.InvokeTargetShadow
---

# IWRdsProtocolShadowCallback::InvokeTargetShadow


## -description

Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

## -parameters

### -param pTargetServerName [in]

A pointer to a string that contains the name of the shadow target server.

### -param TargetSessionId [in]

An integer that specifies the ID of the target session to shadow.

### -param pParam1 [in]

A pointer to a buffer that contains an arbitrary parameter.

### -param Param1Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam1</i> parameter.

### -param pParam2 [in]

A pointer to a buffer that contains an arbitrary parameter.

### -param Param2Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam2</i> parameter.

### -param pParam3 [in]

A pointer to a buffer that contains an arbitrary parameter.

### -param Param3Size [in]

An integer that contains the size, in bytes, of the value referenced by the <i>pParam3</i> parameter.

### -param pParam4 [in]

A pointer to a buffer that contains an arbitrary parameter.

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

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback">IWRdsProtocolShadowCallback</a>