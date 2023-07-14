---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState
title: IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState (wmlss.h)
description: The get_userInternetMediaSharingState method retrieves a value that indicates whether the current user's media library is shared on the Internet.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","get_userInternetMediaSharingState method","IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState","IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState","get_userInternetMediaSharingState","get_userInternetMediaSharingState method [Windows Media Library Sharing Services]","get_userInternetMediaSharingState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSget_userInternetMediaSharingState","wmlss/IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState"]
old-location: wmlss\IWMLSSget_userInternetMediaSharingState.htm
tech.root: WMLSS
ms.assetid: 577fb416-1ff4-4206-8916-9b54577e4cd3
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_userInternetMediaSharingState method, IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState, IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState, get_userInternetMediaSharingState, get_userInternetMediaSharingState method [Windows Media Library Sharing Services], get_userInternetMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_userInternetMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState
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
 - IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState
 - wmlss/IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState
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
 - IWindowsMediaLibrarySharingServices.get_userInternetMediaSharingState
---

# IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_userInternetMediaSharingState</b> method retrieves a value that indicates whether the current user's media library is shared on the Internet.

## -parameters

### -param sharingEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if the media library is shared and <b>VARIANT_FALSE</b> if the media library is not shared.

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

If Internet media sharing is not allowed for the computer, this method retrieves <b>VARIANT_FALSE</b> regardless of whether Internet media sharing is enabled by the current user.

If Internet media sharing is allowed for the computer and Internet media sharing  is enabled by the current user, this method retrieves <b>VARIANT_TRUE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_userinternetmediasharingstate">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState</a>