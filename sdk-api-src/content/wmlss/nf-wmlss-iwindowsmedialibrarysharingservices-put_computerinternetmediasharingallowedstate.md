---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState
title: IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState (wmlss.h)
description: The put_computerInternetMediaSharingAllowedState method specifies whether media libraries on the computer are allowed to be shared on the Internet.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_computerInternetMediaSharingAllowedState method","IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState","IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState","put_computerInternetMediaSharingAllowedState","put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services]","put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_computerInternetMediaSharingAllowedState","wmlss/IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState"]
old-location: wmlss\IWMLSSput_computerInternetMediaSharingAllowedState.htm
tech.root: WMLSS
ms.assetid: d41d63d7-2b15-4dd5-bbc1-17696924a624
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_computerInternetMediaSharingAllowedState method, IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState, IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState, put_computerInternetMediaSharingAllowedState, put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services], put_computerInternetMediaSharingAllowedState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_computerInternetMediaSharingAllowedState, wmlss/IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState
req.header: wmlss.h
req.include-header: Wmlss.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: WMPMediaSharing.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState
 - wmlss/IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMPMediaSharing.dll
api_name:
 - IWindowsMediaLibrarySharingServices.put_computerInternetMediaSharingAllowedState
---

# IWindowsMediaLibrarySharingServices::put_computerInternetMediaSharingAllowedState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_computerInternetMediaSharingAllowedState</b> method specifies whether media libraries on the computer are allowed to be shared on the Internet.

## -parameters

### -param sharingAllowed [in]

A <b>VARIANT_BOOL</b> that specifies whether sharing is allowed (<b>VARIANT_TRUE</b>) or not allowed (<b>VARIANT_FALSE</b>).

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

If home media sharing is not allowed for the computer, Internet media sharing is not allowed for the computer.

If Internet media sharing is not allowed for the computer, none of the users' media libraries are shared on the Internet, regardless of whether individual users have enabled Internet media sharing.

If Internet media sharing is allowed for the computer and a particular user has enabled Internet media sharing, then that user's media library is shared on the Internet.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_computerinternetmediasharingallowedstate">IWindowsMediaLibrarySharingServices::get_computerInternetMediaSharingAllowedState</a>