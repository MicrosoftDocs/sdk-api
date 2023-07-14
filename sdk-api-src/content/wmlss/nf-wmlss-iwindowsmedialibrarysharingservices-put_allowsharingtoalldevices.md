---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices
title: IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices (wmlss.h)
description: The put_allowSharingToAllDevices method allows or disallows sharing of the current user's media library with all devices on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","put_allowSharingToAllDevices method","IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices","IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices","put_allowSharingToAllDevices","put_allowSharingToAllDevices method [Windows Media Library Sharing Services]","put_allowSharingToAllDevices method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSput_allowSharingToAllDevices","wmlss/IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices"]
old-location: wmlss\IWMLSSput_allowSharingToAllDevices.htm
tech.root: WMLSS
ms.assetid: c0dbc9ce-de09-4f60-a975-f09367ba9145
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],put_allowSharingToAllDevices method, IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices, IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices, put_allowSharingToAllDevices, put_allowSharingToAllDevices method [Windows Media Library Sharing Services], put_allowSharingToAllDevices method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSput_allowSharingToAllDevices, wmlss/IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices
 - wmlss/IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices
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
 - IWindowsMediaLibrarySharingServices.put_allowSharingToAllDevices
---

# IWindowsMediaLibrarySharingServices::put_allowSharingToAllDevices


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_allowSharingToAllDevices</b> method allows or disallows sharing of the current user's media library with all devices on the home network.

## -parameters

### -param sharingEnabled [in]

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

