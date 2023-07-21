---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices
title: IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices (wmlss.h)
description: The get_allowSharingToAllDevices method retrieves a value that indicates whether the current user's media library is shared with all devices on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","get_allowSharingToAllDevices method","IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices","IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices","get_allowSharingToAllDevices","get_allowSharingToAllDevices method [Windows Media Library Sharing Services]","get_allowSharingToAllDevices method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSget_allowSharingToAllDevices","wmlss/IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices"]
old-location: wmlss\IWMLSSget_allowSharingToAllDevices.htm
tech.root: WMLSS
ms.assetid: f166eca1-9413-4f14-be2f-ef433f3e391a
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],get_allowSharingToAllDevices method, IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices, IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices, get_allowSharingToAllDevices, get_allowSharingToAllDevices method [Windows Media Library Sharing Services], get_allowSharingToAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSget_allowSharingToAllDevices, wmlss/IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices
 - wmlss/IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices.get_allowSharingToAllDevices
---

# IWindowsMediaLibrarySharingServices::get_allowSharingToAllDevices


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_allowSharingToAllDevices</b> method retrieves a value that indicates whether the current user's media library is shared with all devices on the home network.

## -parameters

### -param sharingEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if the media library is shared with all devices and <b>VARIANT_FALSE</b> if the media library is not shared with at least one device.

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

