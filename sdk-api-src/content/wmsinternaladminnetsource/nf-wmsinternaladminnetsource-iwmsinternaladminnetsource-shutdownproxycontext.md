---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.ShutdownProxyContext
title: IWMSInternalAdminNetSource::ShutdownProxyContext (wmsinternaladminnetsource.h)
description: The ShutdownProxyContext method releases the internal resources used by IWMSInternalAdminNetSource::FindProxyForURL. To avoid memory leaks, you must call this method after you are finished making calls to FindProxyForURL.
helpviewer_keywords: ["IWMSInternalAdminNetSource interface [windows Media Format]","ShutdownProxyContext method","IWMSInternalAdminNetSource.ShutdownProxyContext","IWMSInternalAdminNetSource::ShutdownProxyContext","IWMSInternalAdminNetSourceShutdownProxyContext","ShutdownProxyContext","ShutdownProxyContext method [windows Media Format]","ShutdownProxyContext method [windows Media Format]","IWMSInternalAdminNetSource interface","wmformat.iwmsinternaladminnetsource_shutdownproxycontext","wmsinternaladminnetsource/IWMSInternalAdminNetSource::ShutdownProxyContext"]
old-location: wmformat\iwmsinternaladminnetsource_shutdownproxycontext.htm
tech.root: wmformat
ms.assetid: 95c6f641-e0b1-4391-b4bd-b43c03a330b4
ms.date: 4/26/2023
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],ShutdownProxyContext method, IWMSInternalAdminNetSource.ShutdownProxyContext, IWMSInternalAdminNetSource::ShutdownProxyContext, IWMSInternalAdminNetSourceShutdownProxyContext, ShutdownProxyContext, ShutdownProxyContext method [windows Media Format], ShutdownProxyContext method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_shutdownproxycontext, wmsinternaladminnetsource/IWMSInternalAdminNetSource::ShutdownProxyContext
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
 - IWMSInternalAdminNetSource::ShutdownProxyContext
 - wmsinternaladminnetsource/IWMSInternalAdminNetSource::ShutdownProxyContext
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
 - IWMSInternalAdminNetSource.ShutdownProxyContext
---

# IWMSInternalAdminNetSource::ShutdownProxyContext


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ShutdownProxyContext</b> method releases the internal resources used by <a href="/windows/desktop/api/wmsinternaladminnetsource/nf-wmsinternaladminnetsource-iwmsinternaladminnetsource-findproxyforurl">IWMSInternalAdminNetSource::FindProxyForURL</a>. To avoid memory leaks, you must call this method after you are finished making calls to <b>FindProxyForURL</b>.

## -parameters

### -param dwProxyContext [in]

<b>DWORD</b> containing the proxy context. Set this to the last proxy context received from <b>FindProxyForURL</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsinternaladminnetsource/nn-wmsinternaladminnetsource-iwmsinternaladminnetsource">IWMSInternalAdminNetSource Interface</a>