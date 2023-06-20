---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.ResetLoggingUrlList
title: IWMReaderNetworkConfig::ResetLoggingUrlList (wmsdkidl.h)
description: The ResetLoggingUrlList method clears the list of servers that receive logging data.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","ResetLoggingUrlList method","IWMReaderNetworkConfig.ResetLoggingUrlList","IWMReaderNetworkConfig::ResetLoggingUrlList","IWMReaderNetworkConfigResetLoggingUrlList","ResetLoggingUrlList","ResetLoggingUrlList method [windows Media Format]","ResetLoggingUrlList method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_resetloggingurllist","wmsdkidl/IWMReaderNetworkConfig::ResetLoggingUrlList"]
old-location: wmformat\iwmreadernetworkconfig_resetloggingurllist.htm
tech.root: wmformat
ms.assetid: 0fe71d73-a827-4aed-a37b-db7701cc1180
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],ResetLoggingUrlList method, IWMReaderNetworkConfig.ResetLoggingUrlList, IWMReaderNetworkConfig::ResetLoggingUrlList, IWMReaderNetworkConfigResetLoggingUrlList, ResetLoggingUrlList, ResetLoggingUrlList method [windows Media Format], ResetLoggingUrlList method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_resetloggingurllist, wmsdkidl/IWMReaderNetworkConfig::ResetLoggingUrlList
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig::ResetLoggingUrlList
 - wmsdkidl/IWMReaderNetworkConfig::ResetLoggingUrlList
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
 - IWMReaderNetworkConfig.ResetLoggingUrlList
---

# IWMReaderNetworkConfig::ResetLoggingUrlList


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ResetLoggingUrlList</b> method clears the list of servers that receive logging data.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method removes any servers that were added using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl">IWMReaderNetworkConfig::AddLoggingUrl</a> method. Note that the originating server always receives a log, even after the list is cleared.

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>
