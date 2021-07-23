---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.RegisterProxyFailure
title: IWMSInternalAdminNetSource::RegisterProxyFailure (wmsinternaladminnetsource.h)
description: Registers a proxy failure.
helpviewer_keywords: ["IWMSInternalAdminNetSource interface [windows Media Format]","RegisterProxyFailure method","IWMSInternalAdminNetSource.RegisterProxyFailure","IWMSInternalAdminNetSource::RegisterProxyFailure","RegisterProxyFailure","RegisterProxyFailure method [windows Media Format]","RegisterProxyFailure method [windows Media Format]","IWMSInternalAdminNetSource interface","wmformat.iwmsinternaladminnetsource_registerproxyfailure","wmsinternaladminnetsource/IWMSInternalAdminNetSource::RegisterProxyFailure"]
old-location: wmformat\iwmsinternaladminnetsource_registerproxyfailure.htm
tech.root: wmformat
ms.assetid: 50a41a98-2827-425e-91fc-5196996abe98
ms.date: 12/05/2018
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],RegisterProxyFailure method, IWMSInternalAdminNetSource.RegisterProxyFailure, IWMSInternalAdminNetSource::RegisterProxyFailure, RegisterProxyFailure, RegisterProxyFailure method [windows Media Format], RegisterProxyFailure method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_registerproxyfailure, wmsinternaladminnetsource/IWMSInternalAdminNetSource::RegisterProxyFailure
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMSInternalAdminNetSource::RegisterProxyFailure
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource::RegisterProxyFailure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSInternalAdminNetSource.RegisterProxyFailure
---

# IWMSInternalAdminNetSource::RegisterProxyFailure


## -description

Registers a proxy failure.

## -parameters

### -param hrParam [in]

The <b>HRESULT</b> code of  the failure.

### -param dwProxyContext [in]

Represents the proxy server.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>