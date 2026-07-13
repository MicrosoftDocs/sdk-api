---
UID: NF:wmp.IWMPCdromBurn.get_burnProgress
title: IWMPCdromBurn::get_burnProgress (wmp.h)
description: The get_burnProgress method retrieves the CD burning progress as percent complete.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","get_burnProgress method","IWMPCdromBurn.get_burnProgress","IWMPCdromBurn::get_burnProgress","IWMPCdromBurnget_burnProgress","get_burnProgress","get_burnProgress method [Windows Media Player]","get_burnProgress method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_get_burnprogress","wmp/IWMPCdromBurn::get_burnProgress"]
old-location: wmp\iwmpcdromburn_get_burnprogress.htm
tech.root: WMP
ms.assetid: 4941e1be-1ed2-4d8e-ad16-79ddbdcd71bf
ms.date: 4/26/2023
ms.keywords: IWMPCdromBurn interface [Windows Media Player],get_burnProgress method, IWMPCdromBurn.get_burnProgress, IWMPCdromBurn::get_burnProgress, IWMPCdromBurnget_burnProgress, get_burnProgress, get_burnProgress method [Windows Media Player], get_burnProgress method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_get_burnprogress, wmp/IWMPCdromBurn::get_burnProgress
req.header: wmp.h
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
 - IWMPCdromBurn::get_burnProgress
 - wmp/IWMPCdromBurn::get_burnProgress
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
 - IWMPCdromBurn.get_burnProgress
---

# IWMPCdromBurn::get_burnProgress


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_burnProgress</b> method retrieves the CD burning progress as percent complete.

## -parameters

### -param plProgress [out]

Pointer to a <b>long</b> that receives the progress value. Progress values range from 0 to 100.

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

The progress value represents the completed percentage of the entire burning process, including any staging operations.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>