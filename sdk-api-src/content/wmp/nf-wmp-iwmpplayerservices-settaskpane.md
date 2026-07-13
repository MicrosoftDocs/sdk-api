---
UID: NF:wmp.IWMPPlayerServices.setTaskPane
title: IWMPPlayerServices::setTaskPane (wmp.h)
description: The setTaskPane method displays the specified task pane in the full mode of Windows Media Player.
helpviewer_keywords: ["IWMPPlayerServices interface [Windows Media Player]","setTaskPane method","IWMPPlayerServices.setTaskPane","IWMPPlayerServices::setTaskPane","IWMPPlayerServicessetTaskPane","setTaskPane","setTaskPane method [Windows Media Player]","setTaskPane method [Windows Media Player]","IWMPPlayerServices interface","wmp.iwmpplayerservices_settaskpane","wmp/IWMPPlayerServices::setTaskPane"]
old-location: wmp\iwmpplayerservices_settaskpane.htm
tech.root: WMP
ms.assetid: 4b34ec95-d9a3-4135-b369-39955199ac00
ms.date: 4/26/2023
ms.keywords: IWMPPlayerServices interface [Windows Media Player],setTaskPane method, IWMPPlayerServices.setTaskPane, IWMPPlayerServices::setTaskPane, IWMPPlayerServicessetTaskPane, setTaskPane, setTaskPane method [Windows Media Player], setTaskPane method [Windows Media Player],IWMPPlayerServices interface, wmp.iwmpplayerservices_settaskpane, wmp/IWMPPlayerServices::setTaskPane
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
 - IWMPPlayerServices::setTaskPane
 - wmp/IWMPPlayerServices::setTaskPane
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
 - IWMPPlayerServices.setTaskPane
---

# IWMPPlayerServices::setTaskPane


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setTaskPane</b> method displays the specified task pane in the full mode of Windows Media Player.

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
<td>NowPlaying</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the<b> Now Playing</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Player</b> mode .

</td>
</tr>
<tr>
<td>MediaGuide</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the <b>Media Guide</b> feature. 

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the Media Guide displayed.

</td>
</tr>
<tr>
<td>CopyFromCD</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy From CD</b> feature.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Rip</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode.

</td>
</tr>
<tr>
<td>CopyFromCD?AutoCopy:<i>id</i></td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy From CD</b> feature and automatically invokes the copy functionality after switching.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Rip</b> feature and automatically invokes the rip functionality after switching.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode and automatically invokes the rip functionality after switching.

All versions: To specify a particular drive identifier, append a colon character (:) followed by the CD drive identifier number. If you omit the colon and the ID, the first CD drive is  used. If the user has selected <b>Eject CD when copying is completed</b> in Windows Media Player, the CD will be ejected when copying is completed.

</td>
</tr>
<tr>
<td>Library</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the <b>Library</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the <b>Play</b> tab open.

</td>
</tr>
<tr>
<td>RadioTuner</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Radio Tuner</b> feature

Windows Media Player 10, 11, 12: Opens Windows Media Player in the current active online store.

</td>
</tr>
<tr>
<td>CopyToCD</td>
<td>
Windows Media Player 9: Not supported.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Burn</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the burn list open.

</td>
</tr>
<tr>
<td>CopyToCDOrDevice</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy to CD or Device</b> feature.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Sync</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the <b>Sync</b> tab open.

</td>
</tr>
<tr>
<td>Services</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Premium Services</b> feature 

Windows Media Player 10, 11, 12: Opens Windows Media Player in the current active online store.

</td>
</tr>
<tr>
<td>SkinChooser</td>
<td>
Opens Windows Media Player in the <b>Skin Chooser</b> feature.

</td>
</tr>
</table>

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

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpaneurl">IWMPPlayerServices::setTaskPaneURL(deprecated)</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices">IWMPPlayerServicesInterface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>