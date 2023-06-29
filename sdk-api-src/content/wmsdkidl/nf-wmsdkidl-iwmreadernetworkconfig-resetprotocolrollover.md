---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.ResetProtocolRollover
title: IWMReaderNetworkConfig::ResetProtocolRollover (wmsdkidl.h)
description: The ResetProtocolRollover method forces the reader object to use the normal protocol rollover algorithm.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","ResetProtocolRollover method","IWMReaderNetworkConfig.ResetProtocolRollover","IWMReaderNetworkConfig::ResetProtocolRollover","IWMReaderNetworkConfigResetProtocolRollover","ResetProtocolRollover","ResetProtocolRollover method [windows Media Format]","ResetProtocolRollover method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_resetprotocolrollover","wmsdkidl/IWMReaderNetworkConfig::ResetProtocolRollover"]
old-location: wmformat\iwmreadernetworkconfig_resetprotocolrollover.htm
tech.root: wmformat
ms.assetid: 10a11131-48bd-49bd-a767-1c6148f84b95
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],ResetProtocolRollover method, IWMReaderNetworkConfig.ResetProtocolRollover, IWMReaderNetworkConfig::ResetProtocolRollover, IWMReaderNetworkConfigResetProtocolRollover, ResetProtocolRollover, ResetProtocolRollover method [windows Media Format], ResetProtocolRollover method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_resetprotocolrollover, wmsdkidl/IWMReaderNetworkConfig::ResetProtocolRollover
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
 - IWMReaderNetworkConfig::ResetProtocolRollover
 - wmsdkidl/IWMReaderNetworkConfig::ResetProtocolRollover
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
 - IWMReaderNetworkConfig.ResetProtocolRollover
---

# IWMReaderNetworkConfig::ResetProtocolRollover


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ResetProtocolRollover</b> method forces the reader object to use the normal protocol rollover algorithm.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Protocol rollover is a process whereby the reader object discovers the best streaming protocol available from a server. For more information, see <a href="/windows/desktop/wmformat/protocol-rollover">Protocol Rollover</a>.

When the reader object uses protocol rollover, it records which protocol was used and tries that protocol first on subsequent connection attempts. After a certain period of time, the reader object goes back to the default protocol rollover behavior.

However, if the application disables a particular protocol (for example, by calling <b>SetEnableUDP</b> or <b>SetEnableTCP</b>), the reader object may use a protocol that is less efficient than necessary. You can force the reader object to use the default protocol rollover behavior by calling the <b>ResetProtocolRollover</b> method.

Player users sometimes experiment with network settings when they are having connectivity problems. By using this method to reset the protocol rollover settings, the application can improve the quality of streaming that users receive.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp">IWMReaderNetworkConfig::SetEnableUDP</a>
