---
UID: NF:wmp.IWMPCore.launchURL
title: IWMPCore::launchURL (wmp.h)
description: The launchURL method sends a URL to the user's default browser.
helpviewer_keywords: ["IWMPCore interface [Windows Media Player]","launchURL method","IWMPCore.launchURL","IWMPCore::launchURL","IWMPCorelaunchURL","launchURL","launchURL method [Windows Media Player]","launchURL method [Windows Media Player]","IWMPCore interface","wmp.iwmpcore_launchurl","wmp/IWMPCore::launchURL"]
old-location: wmp\iwmpcore_launchurl.htm
tech.root: WMP
ms.assetid: 439bb4a7-801a-4bef-b791-b8a9cb24ab34
ms.date: 4/26/2023
ms.keywords: IWMPCore interface [Windows Media Player],launchURL method, IWMPCore.launchURL, IWMPCore::launchURL, IWMPCorelaunchURL, launchURL, launchURL method [Windows Media Player], launchURL method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_launchurl, wmp/IWMPCore::launchURL
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
 - IWMPCore::launchURL
 - wmp/IWMPCore::launchURL
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
 - IWMPCore.launchURL
---

# IWMPCore::launchURL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>launchURL</b> method sends a URL to the user's default browser.

## -parameters

### -param bstrURL [in]

<b>BSTR</b> containing the URL.

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

This method only opens webpages using the HTTP or HTTPS protocols.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>