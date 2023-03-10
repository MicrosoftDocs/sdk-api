---
UID: NF:wsmandisp.IWSManConnectionOptionsEx2.ProxyNoProxyServer
title: IWSManConnectionOptionsEx2::ProxyNoProxyServer (wsmandisp.h)
description: Returns the value of the proxy access type flag WSManProxyNoProxyServer for use in the accessType parameter of the IWSManConnectionOptionsEx2::SetProxy method.
helpviewer_keywords: ["IWSManConnectionOptionsEx2 interface [Windows Remote Management]","ProxyNoProxyServer method","IWSManConnectionOptionsEx2.ProxyNoProxyServer","IWSManConnectionOptionsEx2::ProxyNoProxyServer","ProxyNoProxyServer","ProxyNoProxyServer method [Windows Remote Management]","ProxyNoProxyServer method [Windows Remote Management]","IWSManConnectionOptionsEx2 interface","winrm.iwsmanconnectionoptionsex2_proxynoproxyserver","wsmandisp/IWSManConnectionOptionsEx2::ProxyNoProxyServer"]
old-location: winrm\iwsmanconnectionoptionsex2_proxynoproxyserver.htm
tech.root: winrm
ms.assetid: 00613052-7428-4719-9a19-fc27541af07a
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptionsEx2 interface [Windows Remote Management],ProxyNoProxyServer method, IWSManConnectionOptionsEx2.ProxyNoProxyServer, IWSManConnectionOptionsEx2::ProxyNoProxyServer, ProxyNoProxyServer, ProxyNoProxyServer method [Windows Remote Management], ProxyNoProxyServer method [Windows Remote Management],IWSManConnectionOptionsEx2 interface, winrm.iwsmanconnectionoptionsex2_proxynoproxyserver, wsmandisp/IWSManConnectionOptionsEx2::ProxyNoProxyServer
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - IWSManConnectionOptionsEx2::ProxyNoProxyServer
 - wsmandisp/IWSManConnectionOptionsEx2::ProxyNoProxyServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSManDisp.h
api_name:
 - IWSManConnectionOptionsEx2.ProxyNoProxyServer
---

# IWSManConnectionOptionsEx2::ProxyNoProxyServer


## -description

Returns the value of the proxy access type flag <b>WSManProxyNoProxyServer</b> for use in the <i>accessType</i> parameter of the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">IWSManConnectionOptionsEx2::SetProxy</a> method.

## -parameters

### -param value [out, retval]

Specifies the value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptionsex2">IWSManConnectionOptionsEx2</a>