---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.setAuthorizationState
title: IWindowsMediaLibrarySharingServices::setAuthorizationState (wmlss.h)
description: The setAuthorizationState method enables or disables access to the current user's media library by a specified device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","setAuthorizationState method","IWindowsMediaLibrarySharingServices.setAuthorizationState","IWindowsMediaLibrarySharingServices::setAuthorizationState","setAuthorizationState","setAuthorizationState method [Windows Media Library Sharing Services]","setAuthorizationState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSsetAuthorizationState","wmlss/IWindowsMediaLibrarySharingServices::setAuthorizationState"]
old-location: wmlss\IWMLSSsetAuthorizationState.htm
tech.root: WMLSS
ms.assetid: bd67b81c-9810-4f35-b0b2-c471b4747216
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],setAuthorizationState method, IWindowsMediaLibrarySharingServices.setAuthorizationState, IWindowsMediaLibrarySharingServices::setAuthorizationState, setAuthorizationState, setAuthorizationState method [Windows Media Library Sharing Services], setAuthorizationState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSsetAuthorizationState, wmlss/IWindowsMediaLibrarySharingServices::setAuthorizationState
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
 - IWindowsMediaLibrarySharingServices::setAuthorizationState
 - wmlss/IWindowsMediaLibrarySharingServices::setAuthorizationState
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
 - IWindowsMediaLibrarySharingServices.setAuthorizationState
---

# IWindowsMediaLibrarySharingServices::setAuthorizationState


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setAuthorizationState</b> method enables or disables access to the current user's media library by  a specified device.

## -parameters

### -param MACAddress [in]

A <b>BSTR</b> that specifies the MAC address of the device for which access will be enabled or disabled.

### -param authorizationState [in]

A <b>VARIANT_BOOL</b> that specifies whether access by the device is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>).

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

## -see-also

<a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-setdefaultauthorization">IWindowsMediaLibrarySharingServices::setDefaultAuthorization</a>