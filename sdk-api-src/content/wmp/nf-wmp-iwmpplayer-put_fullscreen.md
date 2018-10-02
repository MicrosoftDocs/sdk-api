---
UID: NF:wmp.IWMPPlayer.put_fullScreen
title: IWMPPlayer::put_fullScreen
author: windows-sdk-content
description: The put_fullScreen method specifies a value indicating whether video content is played back in full-screen mode.
old-location: wmp\iwmpplayer_put_fullscreen.htm
tech.root: WMP
ms.assetid: 50ce0115-9e49-4431-b818-35bdc34da9a0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPPlayer interface [Windows Media Player],put_fullScreen method, IWMPPlayer.put_fullScreen, IWMPPlayer::put_fullScreen, IWMPPlayerput_fullScreen, put_fullScreen, put_fullScreen method [Windows Media Player], put_fullScreen method [Windows Media Player],IWMPPlayer interface, wmp.iwmpplayer_put_fullscreen, wmp/IWMPPlayer::put_fullScreen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPPlayer.put_fullScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPPlayer::put_fullScreen


## -description



The <b>put_fullScreen</b> method specifies a value indicating whether video content is played back in full-screen mode.




## -parameters




### -param bFullScreen [in]

<b>VARIANT_BOOL</b> indicating whether video content is played back in full-screen mode. The default is <b>FALSE</b>.


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



For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel. If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "mini" or "full", the height of the control itself must be 65 pixels or greater to accommodate the video display area in addition to the user interface.

If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "invisible", then specifying the <b>VARIANT_BOOL</b> to <b>TRUE</b> in <b>IWMPPlayer::get_fullScreen</b> raises an error and does not affect the behavior of the control.

During full-screen playback, Windows Media Player hides the mouse cursor when the <b>VARIANT_BOOL</b> retrieved from <b>IWMPPlayer::get_enableContextMenu</b> equals <b>FALSE</b> and the <b>BSTR</b> retrieved from <b>IWMPPlayer::get_uiMode</b> equals "none".

If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves. After a brief interval of no mouse movement, the transport controls are hidden. If the <b>BSTR</b> specified in <b>IWMPPlayer::put_uiMode</b> is set to "none", no controls are displayed in full-screen mode.

Note
        

Displaying transport controls in full-screen mode requires the Windows XP operating system.

If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.




## -see-also




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/66769441-7923-45d2-b84f-24770537923c">IWMPPlayer::get_enableContextMenu</a>



<a href="https://msdn.microsoft.com/5a8bb0b5-76c6-424f-ba37-5e913b6ed542">IWMPPlayer::get_fullScreen</a>



<a href="https://msdn.microsoft.com/154db914-a0c3-44de-b692-e1b7f9c681f6">IWMPPlayer::put_uiMode</a>
 

 

