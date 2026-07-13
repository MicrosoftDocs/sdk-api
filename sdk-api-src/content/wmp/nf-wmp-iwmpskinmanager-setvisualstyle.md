---
UID: NF:wmp.IWMPSkinManager.SetVisualStyle
title: IWMPSkinManager::SetVisualStyle (wmp.h)
description: The SetVisualStyle method specifies the path to a theme file in Windows XP to which Windows Media Player synchronizes the skin.
helpviewer_keywords: ["IWMPSkinManager interface [Windows Media Player]","SetVisualStyle method","IWMPSkinManager.SetVisualStyle","IWMPSkinManager::SetVisualStyle","IWMPSkinManagerSetVisualStyle","SetVisualStyle","SetVisualStyle method [Windows Media Player]","SetVisualStyle method [Windows Media Player]","IWMPSkinManager interface","wmp.iwmpskinmanager_setvisualstyle","wmp/IWMPSkinManager::SetVisualStyle"]
old-location: wmp\iwmpskinmanager_setvisualstyle.htm
tech.root: WMP
ms.assetid: 16d0020f-7650-4300-bd34-6f79ecca5175
ms.date: 4/26/2023
ms.keywords: IWMPSkinManager interface [Windows Media Player],SetVisualStyle method, IWMPSkinManager.SetVisualStyle, IWMPSkinManager::SetVisualStyle, IWMPSkinManagerSetVisualStyle, SetVisualStyle, SetVisualStyle method [Windows Media Player], SetVisualStyle method [Windows Media Player],IWMPSkinManager interface, wmp.iwmpskinmanager_setvisualstyle, wmp/IWMPSkinManager::SetVisualStyle
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
 - IWMPSkinManager::SetVisualStyle
 - wmp/IWMPSkinManager::SetVisualStyle
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
 - IWMPSkinManager.SetVisualStyle
---

# IWMPSkinManager::SetVisualStyle


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetVisualStyle</b> method specifies the path to a theme file in Windows XP to which Windows Media Player synchronizes the skin.

## -parameters

### -param bstrPath [in]

<b>BSTR</b> containing the path to the theme file.

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

Windows XP calls this method when the user changes the current theme. The current skin selection will change to match the theme, or will change to the Windows Classic skin if there is no skin that matches the current theme. If Windows Media Player is in skin mode, the skin will change immediately. Otherwise, the new skin selection will be applied the next time skin mode is entered.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager">IWMPSkinManager Interface</a>