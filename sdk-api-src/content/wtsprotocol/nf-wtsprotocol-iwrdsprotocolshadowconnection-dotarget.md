---
UID: NF:wtsprotocol.IWRdsProtocolShadowConnection.DoTarget
title: IWRdsProtocolShadowConnection::DoTarget (wtsprotocol.h)
description: Requests that the protocol start the target side of a shadow connection.
helpviewer_keywords: ["DoTarget","DoTarget method [Remote Desktop Services]","DoTarget method [Remote Desktop Services]","IWRdsProtocolShadowConnection interface","IWRdsProtocolShadowConnection interface [Remote Desktop Services]","DoTarget method","IWRdsProtocolShadowConnection.DoTarget","IWRdsProtocolShadowConnection::DoTarget","termserv.iwrdsprotocolshadowconnection_dotarget","wtsprotocol/IWRdsProtocolShadowConnection::DoTarget"]
old-location: termserv\iwrdsprotocolshadowconnection_dotarget.htm
tech.root: TermServ
ms.assetid: 9fe2e3fb-f368-4b7e-b679-402db900916c
ms.date: 12/05/2018
ms.keywords: DoTarget, DoTarget method [Remote Desktop Services], DoTarget method [Remote Desktop Services],IWRdsProtocolShadowConnection interface, IWRdsProtocolShadowConnection interface [Remote Desktop Services],DoTarget method, IWRdsProtocolShadowConnection.DoTarget, IWRdsProtocolShadowConnection::DoTarget, termserv.iwrdsprotocolshadowconnection_dotarget, wtsprotocol/IWRdsProtocolShadowConnection::DoTarget
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
 - IWRdsProtocolShadowConnection::DoTarget
 - wtsprotocol/IWRdsProtocolShadowConnection::DoTarget
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
 - IWRdsProtocolShadowConnection.DoTarget
---

# IWRdsProtocolShadowConnection::DoTarget


## -description

Requests that the protocol start the target side of a shadow connection.

## -parameters

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

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The four parameters <i>pParam1</i>, <i>pParam2</i>, <i>pParam3</i>, and <i>pParam4</i> can contain any information that must be exchanged between the shadow client and the shadow target. The Remote Desktop Services service passes the information through without modification.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a>