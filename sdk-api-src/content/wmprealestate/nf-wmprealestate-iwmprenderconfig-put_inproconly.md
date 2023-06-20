---
UID: NF:wmprealestate.IWMPRenderConfig.put_inProcOnly
title: IWMPRenderConfig::put_inProcOnly (wmprealestate.h)
description: The put_inProcOnly method specifies a value indicating whether playback is restricted to the current process.
helpviewer_keywords: ["IWMPRenderConfig interface [Windows Media Player]","put_inProcOnly method","IWMPRenderConfig.put_inProcOnly","IWMPRenderConfig::put_inProcOnly","IWMPRenderConfigputInProcOnly","put_inProcOnly","put_inProcOnly method [Windows Media Player]","put_inProcOnly method [Windows Media Player]","IWMPRenderConfig interface","wmp.iwmprenderconfig_put_inproconly","wmprealestate/IWMPRenderConfig::put_inProcOnly"]
old-location: wmp\iwmprenderconfig_put_inproconly.htm
tech.root: WMP
ms.assetid: fd7c7cbc-f428-46e1-b239-74b78cbf5835
ms.date: 4/26/2023
ms.keywords: IWMPRenderConfig interface [Windows Media Player],put_inProcOnly method, IWMPRenderConfig.put_inProcOnly, IWMPRenderConfig::put_inProcOnly, IWMPRenderConfigputInProcOnly, put_inProcOnly, put_inProcOnly method [Windows Media Player], put_inProcOnly method [Windows Media Player],IWMPRenderConfig interface, wmp.iwmprenderconfig_put_inproconly, wmprealestate/IWMPRenderConfig::put_inProcOnly
req.header: wmprealestate.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPRenderConfig::put_inProcOnly
 - wmprealestate/IWMPRenderConfig::put_inProcOnly
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
 - IWMPRenderConfig.put_inProcOnly
---

# IWMPRenderConfig::put_inProcOnly


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_inProcOnly</b> method specifies a value indicating whether playback is restricted to the current process.

## -parameters

### -param fInProc [in]

<b>BOOL</b>, <b>TRUE</b> specifying that playback is restricted to the current process.

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

Using this method with protected content is not supported.

This method can be helpful when debugging. If your program works with the Media Foundation topology directly (for example, specifying an EVR presenter by using the <a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig">IWMPVideoRenderConfig</a> interface), it might be easier to debug your code when the presenter is in the same process.

This method might also be useful if your Media Foundation components are designed to run in the main program's process.

Note that DirectShow graphs in Windows Media Player always run in the main process.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig">IWMPRenderConfig Interface</a>