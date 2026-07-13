---
UID: NF:wmp.IWMPNetwork.setProxySettings
title: IWMPNetwork::setProxySettings (wmp.h)
description: The setProxySettings method specifies the proxy setting for a given protocol.
helpviewer_keywords: ["IWMPNetwork interface [Windows Media Player]","setProxySettings method","IWMPNetwork.setProxySettings","IWMPNetwork::setProxySettings","IWMPNetworksetProxySettings","setProxySettings","setProxySettings method [Windows Media Player]","setProxySettings method [Windows Media Player]","IWMPNetwork interface","wmp.iwmpnetwork_setproxysettings","wmp/IWMPNetwork::setProxySettings"]
old-location: wmp\iwmpnetwork_setproxysettings.htm
tech.root: WMP
ms.assetid: 3ce07bf8-8521-4240-9859-3bf790ccbf48
ms.date: 4/26/2023
ms.keywords: IWMPNetwork interface [Windows Media Player],setProxySettings method, IWMPNetwork.setProxySettings, IWMPNetwork::setProxySettings, IWMPNetworksetProxySettings, setProxySettings, setProxySettings method [Windows Media Player], setProxySettings method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_setproxysettings, wmp/IWMPNetwork::setProxySettings
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPNetwork::setProxySettings
 - wmp/IWMPNetwork::setProxySettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPNetwork.setProxySettings
---

# IWMPNetwork::setProxySettings


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setProxySettings</b> method specifies the proxy setting for a given protocol.

## -parameters

### -param bstrProtocol [in]

<b>BSTR</b> containing the protocol name. For a list of supported protocols, see <a href="/windows/desktop/WMP/supported-protocols-and-file-types">Supported Protocols and File Types</a>.

### -param lProxySetting [in]

<b>long</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Do not use a proxy server.</td>
</tr>
<tr>
<td>1</td>
<td>Use the proxy settings of the current browser (only valid for HTTP).</td>
</tr>
<tr>
<td>2</td>
<td>Use the manually specified proxy settings.</td>
</tr>
<tr>
<td>3</td>
<td>Auto-detect the proxy settings.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method fails unless the calling application is running on the local computer or intranet.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpnetwork-getproxysettings">IWMPNetwork::getProxySettings</a>