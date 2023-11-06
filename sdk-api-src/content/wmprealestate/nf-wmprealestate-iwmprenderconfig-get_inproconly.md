---
UID: NF:wmprealestate.IWMPRenderConfig.get_inProcOnly
title: IWMPRenderConfig::get_inProcOnly (wmprealestate.h)
description: The get_inProcOnly method retrieves a value indicating whether playback is restricted to the current process.
helpviewer_keywords: ["IWMPRenderConfig interface [Windows Media Player]","get_inProcOnly method","IWMPRenderConfig.get_inProcOnly","IWMPRenderConfig::get_inProcOnly","IWMPRenderConfiggetInProcOnly","get_inProcOnly","get_inProcOnly method [Windows Media Player]","get_inProcOnly method [Windows Media Player]","IWMPRenderConfig interface","wmp.iwmprenderconfig_get_inproconly","wmprealestate/IWMPRenderConfig::get_inProcOnly"]
old-location: wmp\iwmprenderconfig_get_inproconly.htm
tech.root: WMP
ms.assetid: 71284af6-dc76-4a39-81f4-ed265140aad5
ms.date: 4/26/2023
ms.keywords: IWMPRenderConfig interface [Windows Media Player],get_inProcOnly method, IWMPRenderConfig.get_inProcOnly, IWMPRenderConfig::get_inProcOnly, IWMPRenderConfiggetInProcOnly, get_inProcOnly, get_inProcOnly method [Windows Media Player], get_inProcOnly method [Windows Media Player],IWMPRenderConfig interface, wmp.iwmprenderconfig_get_inproconly, wmprealestate/IWMPRenderConfig::get_inProcOnly
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
 - IWMPRenderConfig::get_inProcOnly
 - wmprealestate/IWMPRenderConfig::get_inProcOnly
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
 - IWMPRenderConfig.get_inProcOnly
---

# IWMPRenderConfig::get_inProcOnly


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_inProcOnly</b> method retrieves a value indicating whether playback is restricted to the current process.

## -parameters

### -param pfInProc [in]

Pointer to a <b>BOOL</b> that receives the result. <b>TRUE</b> specifies that playback is restricted to the current process.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig">IWMPRenderConfig Interface</a>