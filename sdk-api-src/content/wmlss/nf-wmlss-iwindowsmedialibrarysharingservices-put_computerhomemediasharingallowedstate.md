---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_computerHomeMediaSharingAllowedState
title: IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState (wmlss.h)
description: The put_computerHomeMediaSharingAllowedState method specifies whether media libraries on the computer are allowed to be shared on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_computerHomeMediaSharingAllowedState method","IWindowsMediaLibrarySharingServices.put_computerHomeMediaSharingAllowedState","IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState","put_computerHomeMediaSharingAllowedState","put_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services]","put_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_computerHomeMediaSharingAllowedState","wmlss/IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState"]
old-location: wmlss\IWMLSSput_computerHomeMediaSharingAllowedState.htm
tech.root: WMLSS
ms.assetid: f844f79e-ae6f-4f57-abec-2b6d5951961f
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_computerHomeMediaSharingAllowedState method, IWindowsMediaLibrarySharingServices.put_computerHomeMediaSharingAllowedState, IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState, put_computerHomeMediaSharingAllowedState, put_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services], put_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_computerHomeMediaSharingAllowedState, wmlss/IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState
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
 - IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState
 - wmlss/IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState
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
 - IWindowsMediaLibrarySharingServices.put_computerHomeMediaSharingAllowedState
---

# IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_computerHomeMediaSharingAllowedState</b> method specifies whether media libraries on the computer are allowed to be shared on the home network.

## -parameters

### -param sharingAllowed

A <b>VARIANT_BOOL</b> that specifies VARIANT_TRUE if media libraries are allowed to be shared  or <b>VARIANT_FALSE</b> if media libraries are not allowed to be shared.

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

This method must be called by code running under elevated privileges.

If home media sharing is not allowed for the computer, none of the users' media libraries are shared on the home network, regardless of whether individual users have enabled home media sharing.


If home media sharing is allowed for the computer and a particular user has enabled media sharing, then that user's media library is shared on the home network.


<div class="alert"><b>Warning</b>  Each call to <b>put_computerHomeMediaSharingAllowedState</b> with the <i>sharingAllowed</i> parameter set to <b>VARIANT_TRUE</b> updates the access control list (ACL) and last changed time  of each file in the computer's Public Music, Public Pictures, and Public Videos folders. This behavior might change in future versions of Windows.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState</a>