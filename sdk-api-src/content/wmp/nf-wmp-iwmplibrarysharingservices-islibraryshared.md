---
UID: NF:wmp.IWMPLibrarySharingServices.isLibraryShared
title: IWMPLibrarySharingServices::isLibraryShared (wmp.h)
description: The isLibraryShared method retrieves a value indicating whether the user's library is shared.
helpviewer_keywords: ["IWMPLibrarySharingServices interface [Windows Media Player]","isLibraryShared method","IWMPLibrarySharingServices.isLibraryShared","IWMPLibrarySharingServices::isLibraryShared","IWMPLibrarySharingServicesisLibraryShared","isLibraryShared","isLibraryShared method [Windows Media Player]","isLibraryShared method [Windows Media Player]","IWMPLibrarySharingServices interface","wmp.iwmplibrarysharingservices_islibraryshared","wmp/IWMPLibrarySharingServices::isLibraryShared"]
old-location: wmp\iwmplibrarysharingservices_islibraryshared.htm
tech.root: WMP
ms.assetid: fc0a1396-5b43-43dd-9e0d-b5b3a8cf5cdd
ms.date: 4/26/2023
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],isLibraryShared method, IWMPLibrarySharingServices.isLibraryShared, IWMPLibrarySharingServices::isLibraryShared, IWMPLibrarySharingServicesisLibraryShared, isLibraryShared, isLibraryShared method [Windows Media Player], isLibraryShared method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_islibraryshared, wmp/IWMPLibrarySharingServices::isLibraryShared
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
 - IWMPLibrarySharingServices::isLibraryShared
 - wmp/IWMPLibrarySharingServices::isLibraryShared
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
 - IWMPLibrarySharingServices.isLibraryShared
---

# IWMPLibrarySharingServices::isLibraryShared


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>isLibraryShared</b> method retrieves a value indicating whether the user's library is shared.

## -parameters

### -param pvbShared [out]

Pointer to a <b>VARIANT_BOOL</b> that receives the result. <b>VARIANT_TRUE</b> indicates that the user's library is currently shared.

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