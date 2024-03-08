---
UID: NF:wmp.IWMPRemoteMediaServices.GetCustomUIMode
title: IWMPRemoteMediaServices::GetCustomUIMode (wmp.h)
description: The GetCustomUIMode method is called by Windows Media Player to retrieve the location of a skin file to apply to the Windows Media Player control.
helpviewer_keywords: ["GetCustomUIMode","GetCustomUIMode method [Windows Media Player]","GetCustomUIMode method [Windows Media Player]","IWMPRemoteMediaServices interface","IWMPRemoteMediaServices interface [Windows Media Player]","GetCustomUIMode method","IWMPRemoteMediaServices.GetCustomUIMode","IWMPRemoteMediaServices::GetCustomUIMode","IWMPRemoteMediaServicesGetCustomUIMode","wmp.iwmpremotemediaservices_getcustomuimode","wmp/IWMPRemoteMediaServices::GetCustomUIMode"]
old-location: wmp\iwmpremotemediaservices_getcustomuimode.htm
tech.root: WMP
ms.assetid: 892c2513-9ca2-48fe-b745-0fdc0f445871
ms.date: 4/26/2023
ms.keywords: GetCustomUIMode, GetCustomUIMode method [Windows Media Player], GetCustomUIMode method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetCustomUIMode method, IWMPRemoteMediaServices.GetCustomUIMode, IWMPRemoteMediaServices::GetCustomUIMode, IWMPRemoteMediaServicesGetCustomUIMode, wmp.iwmpremotemediaservices_getcustomuimode, wmp/IWMPRemoteMediaServices::GetCustomUIMode
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
 - IWMPRemoteMediaServices::GetCustomUIMode
 - wmp/IWMPRemoteMediaServices::GetCustomUIMode
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
 - IWMPRemoteMediaServices.GetCustomUIMode
---

# IWMPRemoteMediaServices::GetCustomUIMode


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCustomUIMode</b> method is called by Windows Media Player to retrieve the location of a skin file to apply to the Windows Media Player control.

## -parameters

### -param pbstrFile [out]

Pointer to a <b>BSTR</b> containing the location of the skin file.

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

This method allows you to customize the user interface of the embedded control by using Windows Media Player skin technology. Skins used in this way can communicate with the host of the control through a scriptable object retrieved automatically by Windows Media Player through the <b>IWMPRemoteMediaServices::GetScriptableObject</b> method.

To apply a skin file to the embedded control, you must call <b>IWMPPlayer.put_uiMode</b> with a value of "custom". Your implementation of <b>GetCustomUIMode</b> must also return a value of "file://" followed by the path and file name of a skin definition file located on the local computer.

The embedded Windows Media Player control does not have to be remoted to use this method.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getscriptableobject">IWMPRemoteMediaServices::GetScriptableObject</a>



<a href="/windows/desktop/WMP/using-skins-with-the-windows-media-player-control">Using Skins with the Windows Media Player Control</a>