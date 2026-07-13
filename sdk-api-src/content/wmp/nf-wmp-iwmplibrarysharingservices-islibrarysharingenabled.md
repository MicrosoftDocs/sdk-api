---
UID: NF:wmp.IWMPLibrarySharingServices.isLibrarySharingEnabled
title: IWMPLibrarySharingServices::isLibrarySharingEnabled (wmp.h)
description: The isLibrarySharingEnabled method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.
helpviewer_keywords: ["IWMPLibrarySharingServices interface [Windows Media Player]","isLibrarySharingEnabled method","IWMPLibrarySharingServices.isLibrarySharingEnabled","IWMPLibrarySharingServices::isLibrarySharingEnabled","IWMPLibrarySharingServicesisLibrarySharingEnabled","isLibrarySharingEnabled","isLibrarySharingEnabled method [Windows Media Player]","isLibrarySharingEnabled method [Windows Media Player]","IWMPLibrarySharingServices interface","wmp.iwmplibrarysharingservices_islibrarysharingenabled","wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled"]
old-location: wmp\iwmplibrarysharingservices_islibrarysharingenabled.htm
tech.root: WMP
ms.assetid: bd643869-9111-423e-9f9c-7147d1e3c7b8
ms.date: 4/26/2023
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],isLibrarySharingEnabled method, IWMPLibrarySharingServices.isLibrarySharingEnabled, IWMPLibrarySharingServices::isLibrarySharingEnabled, IWMPLibrarySharingServicesisLibrarySharingEnabled, isLibrarySharingEnabled, isLibrarySharingEnabled method [Windows Media Player], isLibrarySharingEnabled method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_islibrarysharingenabled, wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled
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
 - IWMPLibrarySharingServices::isLibrarySharingEnabled
 - wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled
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
 - IWMPLibrarySharingServices.isLibrarySharingEnabled
---

# IWMPLibrarySharingServices::isLibrarySharingEnabled


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>isLibrarySharingEnabled</b> method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.

## -parameters

### -param pvbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives the result. <b>VARIANT_TRUE</b> indicates that the user has enabled library sharing.

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

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices">IWMPLibrarySharingServices Interface</a>