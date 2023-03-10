---
UID: NF:wsmandisp.IWSManConnectionOptionsEx2.ProxyIEConfig
title: IWSManConnectionOptionsEx2::ProxyIEConfig (wsmandisp.h)
description: Returns the value of the proxy access type flag WSManProxyIEConfig for use in the accessType parameter of the IWSManConnectionOptionsEx2::SetProxy method.
helpviewer_keywords: ["IWSManConnectionOptionsEx2 interface [Windows Remote Management]","ProxyIEConfig method","IWSManConnectionOptionsEx2.ProxyIEConfig","IWSManConnectionOptionsEx2::ProxyIEConfig","ProxyIEConfig","ProxyIEConfig method [Windows Remote Management]","ProxyIEConfig method [Windows Remote Management]","IWSManConnectionOptionsEx2 interface","winrm.iwsmanconnectionoptionsex2_proxyieconfig","wsmandisp/IWSManConnectionOptionsEx2::ProxyIEConfig"]
old-location: winrm\iwsmanconnectionoptionsex2_proxyieconfig.htm
tech.root: winrm
ms.assetid: 4aa2bf90-c0e8-400a-a8c7-35656cb3c021
ms.date: 12/05/2018
ms.keywords: IWSManConnectionOptionsEx2 interface [Windows Remote Management],ProxyIEConfig method, IWSManConnectionOptionsEx2.ProxyIEConfig, IWSManConnectionOptionsEx2::ProxyIEConfig, ProxyIEConfig, ProxyIEConfig method [Windows Remote Management], ProxyIEConfig method [Windows Remote Management],IWSManConnectionOptionsEx2 interface, winrm.iwsmanconnectionoptionsex2_proxyieconfig, wsmandisp/IWSManConnectionOptionsEx2::ProxyIEConfig
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
 - IWSManConnectionOptionsEx2::ProxyIEConfig
 - wsmandisp/IWSManConnectionOptionsEx2::ProxyIEConfig
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
 - IWSManConnectionOptionsEx2.ProxyIEConfig
---

# IWSManConnectionOptionsEx2::ProxyIEConfig


## -description

Returns the value of the proxy access type flag <b>WSManProxyIEConfig</b> for use in the <i>accessType</i> parameter of the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy">IWSManConnectionOptionsEx2::SetProxy</a> method.

## -parameters

### -param value [out, retval]

Specifies the value of the constant.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptionsex2">IWSManConnectionOptionsEx2</a>