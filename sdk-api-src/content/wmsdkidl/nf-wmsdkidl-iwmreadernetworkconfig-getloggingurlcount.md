---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetLoggingUrlCount
title: IWMReaderNetworkConfig::GetLoggingUrlCount (wmsdkidl.h)
description: The GetLoggingUrlCount method retrieves the number of URLs in the current list of logging URLs.
helpviewer_keywords: ["GetLoggingUrlCount","GetLoggingUrlCount method [windows Media Format]","GetLoggingUrlCount method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetLoggingUrlCount method","IWMReaderNetworkConfig.GetLoggingUrlCount","IWMReaderNetworkConfig::GetLoggingUrlCount","IWMReaderNetworkConfigGetLoggingUrlCount","wmformat.iwmreadernetworkconfig_getloggingurlcount","wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrlCount"]
old-location: wmformat\iwmreadernetworkconfig_getloggingurlcount.htm
tech.root: wmformat
ms.assetid: 869e093f-8936-4b60-8818-ee2c57924d11
ms.date: 4/26/2023
ms.keywords: GetLoggingUrlCount, GetLoggingUrlCount method [windows Media Format], GetLoggingUrlCount method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetLoggingUrlCount method, IWMReaderNetworkConfig.GetLoggingUrlCount, IWMReaderNetworkConfig::GetLoggingUrlCount, IWMReaderNetworkConfigGetLoggingUrlCount, wmformat.iwmreadernetworkconfig_getloggingurlcount, wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrlCount
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
 - IWMReaderNetworkConfig::GetLoggingUrlCount
 - wmsdkidl/IWMReaderNetworkConfig::GetLoggingUrlCount
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
 - IWMReaderNetworkConfig.GetLoggingUrlCount
---

# IWMReaderNetworkConfig::GetLoggingUrlCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLoggingUrlCount</b> method retrieves the number of URLs in the current list of logging URLs.

## -parameters

### -param pdwUrlCount [out]

Pointer to a <b>DWORD</b> containing the URL count.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getloggingurl">IWMReaderNetworkConfig::GetLoggingUrl</a>