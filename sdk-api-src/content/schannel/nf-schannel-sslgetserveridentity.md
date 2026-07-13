---
UID: NF:schannel.SslGetServerIdentity
title: SslGetServerIdentity function (schannel.h)
description: Gets the identity of the server.
helpviewer_keywords: ["SslGetServerIdentity","SslGetServerIdentity function [Security]","schannel/SslGetServerIdentity","security.sslgetserveridentity"]
old-location: security\sslgetserveridentity.htm
tech.root: security
ms.assetid: 5FA7A0F5-187F-4CE6-AD62-44B71A40568D
ms.date: 12/05/2018
ms.keywords: SslGetServerIdentity, SslGetServerIdentity function [Security], schannel/SslGetServerIdentity, security.sslgetserveridentity
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: schannel.lib
req.dll: Schannel.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SslGetServerIdentity
 - schannel/SslGetServerIdentity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Schannel.dll
api_name:
 - SslGetServerIdentity
---

# SslGetServerIdentity function


## -description

The <b>SslGetServerIdentity</b> function gets the identity of the server. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Schannel.dll.

## -parameters

### -param ClientHello [in]

The message from the client.

### -param ClientHelloSize [in]

The size of the client message.

### -param ServerIdentity [out]

The pointer inside the message where the server name starts.

### -param ServerIdentitySize [out]

The length of the server name.

### -param Flags [in]

This parameter is reserved and must be zero.

## -returns

The status of the call to the function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OK</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters <i>ClientHello</i>, <i>ServerIdentity</i>, or <i>ServerIdentitySize</i> is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INCOMPLETE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The  <i>ServerIdentitySize</i> parameter is smaller than the <i>ClientHelloSize</i> parameter.

</td>
</tr>
</table>