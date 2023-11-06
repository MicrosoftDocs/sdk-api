---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_computerHomeMediaSharingAllowedState
title: IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState (wmlss.h)
description: The get_computerHomeMediaSharingAllowedState method retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","get_computerHomeMediaSharingAllowedState method","IWindowsMediaLibrarySharingServices.get_computerHomeMediaSharingAllowedState","IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState","get_computerHomeMediaSharingAllowedState","get_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services]","get_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSget_computerHomeMediaSharingAllowedState","wmlss/IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState"]
old-location: wmlss\IWMLSSget_computerHomeMediaSharingAllowedState.htm
tech.root: WMLSS
ms.assetid: 9c1ced28-7ed0-4f65-af4d-34774f911621
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_computerHomeMediaSharingAllowedState method, IWindowsMediaLibrarySharingServices.get_computerHomeMediaSharingAllowedState, IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState, get_computerHomeMediaSharingAllowedState, get_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services], get_computerHomeMediaSharingAllowedState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_computerHomeMediaSharingAllowedState, wmlss/IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState
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
 - IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState
 - wmlss/IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState
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
 - IWindowsMediaLibrarySharingServices.get_computerHomeMediaSharingAllowedState
---

# IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_computerHomeMediaSharingAllowedState</b> method retrieves a value that indicates whether media libraries on the computer are allowed to be shared on the home network.

## -parameters

### -param sharingAllowed [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if  media libraries are allowed to be shared and <b>VARIANT_FALSE</b> if media libraries are not allowed to be shared.

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

If home media sharing is not allowed for the computer, none of the users' media libraries are shared on the home network, regardless of whether individual users have enabled home media sharing.

If home media sharing is allowed for the computer and a particular user has enabled media sharing, then that user's media library is shared on the home network.

<div class="alert"><b>Warning</b>  In Windows 7, a call to <b>get_computerHomeMediaSharingAllowedState</b> from a service account might return an incorrect result.</div>
<div> </div>
<div class="alert"><b>Note</b>  Each call to the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState</a> method with the   <i>sharingAllowed</i> parameter set to <b>VARIANT_TRUE</b>   updates the access control list (ACL) and last changed time  for all files in the 

computer's Public Music, Public Pictures, and Public Videos folders.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState</a>