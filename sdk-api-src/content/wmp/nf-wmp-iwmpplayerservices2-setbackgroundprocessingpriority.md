---
UID: NF:wmp.IWMPPlayerServices2.setBackgroundProcessingPriority
title: IWMPPlayerServices2::setBackgroundProcessingPriority (wmp.h)
description: The setBackgroundProcessingPriority method specifies a priority level for general background processing tasks.
helpviewer_keywords: ["IWMPPlayerServices2 interface [Windows Media Player]","setBackgroundProcessingPriority method","IWMPPlayerServices2.setBackgroundProcessingPriority","IWMPPlayerServices2::setBackgroundProcessingPriority","IWMPPlayerServices2setBackgroundProcessingPriority","setBackgroundProcessingPriority","setBackgroundProcessingPriority method [Windows Media Player]","setBackgroundProcessingPriority method [Windows Media Player]","IWMPPlayerServices2 interface","wmp.iwmpplayerservices2_setbackgroundprocessingpriority","wmp/IWMPPlayerServices2::setBackgroundProcessingPriority"]
old-location: wmp\iwmpplayerservices2_setbackgroundprocessingpriority.htm
tech.root: WMP
ms.assetid: 1e3536d2-006b-4019-a9c5-c460135cf555
ms.date: 4/26/2023
ms.keywords: IWMPPlayerServices2 interface [Windows Media Player],setBackgroundProcessingPriority method, IWMPPlayerServices2.setBackgroundProcessingPriority, IWMPPlayerServices2::setBackgroundProcessingPriority, IWMPPlayerServices2setBackgroundProcessingPriority, setBackgroundProcessingPriority, setBackgroundProcessingPriority method [Windows Media Player], setBackgroundProcessingPriority method [Windows Media Player],IWMPPlayerServices2 interface, wmp.iwmpplayerservices2_setbackgroundprocessingpriority, wmp/IWMPPlayerServices2::setBackgroundProcessingPriority
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - IWMPPlayerServices2::setBackgroundProcessingPriority
 - wmp/IWMPPlayerServices2::setBackgroundProcessingPriority
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
 - IWMPPlayerServices2.setBackgroundProcessingPriority
---

# IWMPPlayerServices2::setBackgroundProcessingPriority


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setBackgroundProcessingPriority</b> method specifies a priority level for general background processing tasks.

## -parameters

### -param bstrPriority [in]

<b>BSTR</b> containing one of the following values: "High", "Normal", "Off", or "Urgent".

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

This method is used only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2">IWMPPlayerServices2 Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>