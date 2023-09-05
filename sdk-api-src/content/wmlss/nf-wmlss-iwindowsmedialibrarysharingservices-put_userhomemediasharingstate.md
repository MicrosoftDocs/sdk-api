---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState
title: IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState (wmlss.h)
description: The put_userHomeMediaSharingState method enables or disables sharing of the current user's media library on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_userHomeMediaSharingState method","IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState","IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState","put_userHomeMediaSharingState","put_userHomeMediaSharingState method [Windows Media Library Sharing Services]","put_userHomeMediaSharingState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_userHomeMediaSharingState","wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState"]
old-location: wmlss\IWMLSSput_userHomeMediaSharingState.htm
tech.root: WMLSS
ms.assetid: d638da61-8196-4d46-ad98-fd7ab8a19e9b
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_userHomeMediaSharingState method, IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState, IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState, put_userHomeMediaSharingState, put_userHomeMediaSharingState method [Windows Media Library Sharing Services], put_userHomeMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_userHomeMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState
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
 - IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState
 - wmlss/IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState
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
 - IWindowsMediaLibrarySharingServices.put_userHomeMediaSharingState
---

# IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_userHomeMediaSharingState</b> method enables or disables sharing of the current user's media library on the home network.

## -parameters

### -param sharingEnabled

A <b>VARIANT_BOOL</b> that specifies whether sharing is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>) for the current user.

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

If home media sharing is not allowed for the computer, other users will not have access to the current user's media library, regardless of whether home media sharing is enabled for the current user.



If home media sharing is allowed for the computer and home media sharing is enabled for the current user, other users on the home network will have access to the current user's media library.

<div class="alert"><b>Warning</b>  If home media sharing is enabled for the current user, the computer updates the access control list (ACL) of each file in the user's media library to grant Read access to the NT SERVICE\WMPNetworkSvc account. This behavior might change in future versions of Windows.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_userhomemediasharingstate">IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingStateAllowed</a>