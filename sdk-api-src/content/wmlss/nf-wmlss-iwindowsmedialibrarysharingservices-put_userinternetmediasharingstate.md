---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_userInternetMediaSharingState
title: IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState (wmlss.h)
description: The put_userInternetMediaSharingState method enables or disables sharing of the current user's media library on the Internet.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_userInternetMediaSharingState method","IWindowsMediaLibrarySharingServices.put_userInternetMediaSharingState","IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState","put_userInternetMediaSharingState","put_userInternetMediaSharingState method [Windows Media Library Sharing Services]","put_userInternetMediaSharingState method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_userInternetMediaSharingState","wmlss/IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState"]
old-location: wmlss\IWMLSSput_userInternetMediaSharingState.htm
tech.root: WMLSS
ms.assetid: 3d5ff0eb-02e3-4e03-b606-dcc3a1ec6aaf
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_userInternetMediaSharingState method, IWindowsMediaLibrarySharingServices.put_userInternetMediaSharingState, IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState, put_userInternetMediaSharingState, put_userInternetMediaSharingState method [Windows Media Library Sharing Services], put_userInternetMediaSharingState method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_userInternetMediaSharingState, wmlss/IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState
f1_keywords:
- wmlss/IWindowsMediaLibrarySharingServices.put_userInternetMediaSharingState
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- WMPMediaSharing.dll
api_name:
- IWindowsMediaLibrarySharingServices.put_userInternetMediaSharingState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsMediaLibrarySharingServices::put_userInternetMediaSharingState


## -description


The <b>put_userInternetMediaSharingState</b> method enables or disables sharing of the current user's media library on the Internet.


## -parameters




### -param sharingEnabled

A <b>VARIANT_BOOL</b> that specifies whether sharing on the Internet is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>) for the current user.


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



If Internet media sharing is not allowed for the computer, users on the Internet will not have access to the current user's media library, regardless of whether Internet media sharing is enabled for the current user.

If Internet media sharing is allowed for the computer and Internet media sharing is enabled for the current user, other users on the Internet will have access to the current user's media library.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingservices">IWindowsMediaLibrarySharingServices</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-get_userinternetmediasharingstate">IWindowsMediaLibrarySharingServices::get_userInternetMediaSharingState</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingservices-put_computerhomemediasharingallowedstate">IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState</a>
 

 

