---
UID: NF:wmp.IWMPPlayerServices.setTaskPaneURL
title: IWMPPlayerServices::setTaskPaneURL (wmp.h)
description: This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK. It may be unavailable in subsequent versions.
helpviewer_keywords: ["IWMPPlayerServices interface [Windows Media Player]","setTaskPaneURL method","IWMPPlayerServices.setTaskPaneURL","IWMPPlayerServices::setTaskPaneURL","IWMPPlayerServicessetTaskPaneURLdeprecated","setTaskPaneURL","setTaskPaneURL method [Windows Media Player]","setTaskPaneURL method [Windows Media Player]","IWMPPlayerServices interface","wmp.iwmpplayerservices_settaskpaneurl","wmp/IWMPPlayerServices::setTaskPaneURL"]
old-location: wmp\iwmpplayerservices_settaskpaneurl.htm
tech.root: WMP
ms.assetid: 4ceacaeb-09af-4cdf-84b7-04574a83ec48
ms.date: 4/26/2023
ms.keywords: IWMPPlayerServices interface [Windows Media Player],setTaskPaneURL method, IWMPPlayerServices.setTaskPaneURL, IWMPPlayerServices::setTaskPaneURL, IWMPPlayerServicessetTaskPaneURLdeprecated, setTaskPaneURL, setTaskPaneURL method [Windows Media Player], setTaskPaneURL method [Windows Media Player],IWMPPlayerServices interface, wmp.iwmpplayerservices_settaskpaneurl, wmp/IWMPPlayerServices::setTaskPaneURL
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
 - IWMPPlayerServices::setTaskPaneURL
 - wmp/IWMPPlayerServices::setTaskPaneURL
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
 - IWMPPlayerServices.setTaskPaneURL
---

# IWMPPlayerServices::setTaskPaneURL


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK. It may be unavailable in subsequent versions.
        



The <b>setTaskPaneURL</b> method displays the specified URL in the specified task pane of the full mode of Windows Media Player.

## -parameters

### -param bstrTaskPane [in]

<b>BSTR</b> containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MediaGuide</td>
<td>Opens Windows Media Player in the <b>MediaGuide</b> feature.</td>
</tr>
<tr>
<td>RadioTuner</td>
<td>Opens Windows Media Player in the <b>RadioTuner</b> feature.</td>
</tr>
<tr>
<td>Services</td>
<td>Opens Windows Media Player in the <b>Premium Services</b> feature.</td>
</tr>
</table>

### -param bstrURL [in]

<b>BSTR</b> containing the URL to display in the task pane.

### -param bstrFriendlyName [in]

<b>BSTR</b> containing the friendly name of the content at the specified URL.

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

This method is used only when remoting the Windows Media Player control. This method must be called when the control is in the docked state. Once set, the specified task pane is opened the next time the remoted control transitions to Windows Media Player.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices">IWMPPlayerServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane">IWMPPlayerServices::setTaskPane</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>