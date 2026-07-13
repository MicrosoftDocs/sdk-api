---
UID: NF:wmp.IWMPLibrarySharingServices.showLibrarySharing
title: IWMPLibrarySharingServices::showLibrarySharing (wmp.h)
description: The showLibrarySharing method displays the Windows Media Player Library Sharing dialog box.
helpviewer_keywords: ["IWMPLibrarySharingServices interface [Windows Media Player]","showLibrarySharing method","IWMPLibrarySharingServices.showLibrarySharing","IWMPLibrarySharingServices::showLibrarySharing","IWMPLibrarySharingServicesshowLibrarySharing","showLibrarySharing","showLibrarySharing method [Windows Media Player]","showLibrarySharing method [Windows Media Player]","IWMPLibrarySharingServices interface","wmp.iwmplibrarysharingservices_showlibrarysharing","wmp/IWMPLibrarySharingServices::showLibrarySharing"]
old-location: wmp\iwmplibrarysharingservices_showlibrarysharing.htm
tech.root: WMP
ms.assetid: 87c335ee-c9af-4182-a460-118c53308dad
ms.date: 4/26/2023
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],showLibrarySharing method, IWMPLibrarySharingServices.showLibrarySharing, IWMPLibrarySharingServices::showLibrarySharing, IWMPLibrarySharingServicesshowLibrarySharing, showLibrarySharing, showLibrarySharing method [Windows Media Player], showLibrarySharing method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_showlibrarysharing, wmp/IWMPLibrarySharingServices::showLibrarySharing
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
 - IWMPLibrarySharingServices::showLibrarySharing
 - wmp/IWMPLibrarySharingServices::showLibrarySharing
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
 - IWMPLibrarySharingServices.showLibrarySharing
---

# IWMPLibrarySharingServices::showLibrarySharing


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>showLibrarySharing</b> method displays the Windows Media Player <b>Library Sharing</b> dialog box.



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

The <b>Library Sharing</b> dialog box enables the user to configure library sharing. Users can access this dialog box by pointing to <b>Tools</b>, then clicking <b>Options</b>, and then clicking <b>Configure Media Sharing</b> in the Windows Media Player menu; or by clicking the arrow below the <b>Library</b> tab and then clicking <b>Library Sharing</b>.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices">IWMPLibrarySharingServices Interface</a>
