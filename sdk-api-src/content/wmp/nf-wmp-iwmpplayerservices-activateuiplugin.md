---
UID: NF:wmp.IWMPPlayerServices.activateUIPlugin
title: IWMPPlayerServices::activateUIPlugin (wmp.h)
description: The activateUIPlugin method activates the specified UI plug-in in the full mode of Windows Media Player.
helpviewer_keywords: ["IWMPPlayerServices interface [Windows Media Player]","activateUIPlugin method","IWMPPlayerServices.activateUIPlugin","IWMPPlayerServices::activateUIPlugin","IWMPPlayerServicesactivateUIPlugin","activateUIPlugin","activateUIPlugin method [Windows Media Player]","activateUIPlugin method [Windows Media Player]","IWMPPlayerServices interface","wmp.iwmpplayerservices_activateuiplugin","wmp/IWMPPlayerServices::activateUIPlugin"]
old-location: wmp\iwmpplayerservices_activateuiplugin.htm
tech.root: WMP
ms.assetid: 73274f71-ba34-479c-a23c-38a564e950fa
ms.date: 12/05/2018
ms.keywords: IWMPPlayerServices interface [Windows Media Player],activateUIPlugin method, IWMPPlayerServices.activateUIPlugin, IWMPPlayerServices::activateUIPlugin, IWMPPlayerServicesactivateUIPlugin, activateUIPlugin, activateUIPlugin method [Windows Media Player], activateUIPlugin method [Windows Media Player],IWMPPlayerServices interface, wmp.iwmpplayerservices_activateuiplugin, wmp/IWMPPlayerServices::activateUIPlugin
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
 - IWMPPlayerServices::activateUIPlugin
 - wmp/IWMPPlayerServices::activateUIPlugin
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
 - IWMPPlayerServices.activateUIPlugin
---

# IWMPPlayerServices::activateUIPlugin


## -description

The <b>activateUIPlugin</b> method activates the specified UI plug-in in the full mode of Windows Media Player.

## -parameters

### -param bstrPlugin [in]

<b>BSTR</b> containing the name of the plug-in to activate.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices">IWMPPlayerServices Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>