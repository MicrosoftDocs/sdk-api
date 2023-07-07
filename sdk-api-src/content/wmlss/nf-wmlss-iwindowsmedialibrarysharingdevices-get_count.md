---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevices.get_Count
title: IWindowsMediaLibrarySharingDevices::get_Count (wmlss.h)
description: The get_Count method retrieves the number of media devices on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services]","get_Count method","IWindowsMediaLibrarySharingDevices.get_Count","IWindowsMediaLibrarySharingDevices::get_Count","get_Count","get_Count method [Windows Media Library Sharing Services]","get_Count method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevices interface","wmlss.IWMLSDevicesget_Count","wmlss/IWindowsMediaLibrarySharingDevices::get_Count"]
old-location: wmlss\IWMLSDevicesget_Count.htm
tech.root: WMLSS
ms.assetid: 6eb802a3-18a2-4fcf-9be0-fc251860f3ab
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevices interface [Windows Media Library Sharing Services],get_Count method, IWindowsMediaLibrarySharingDevices.get_Count, IWindowsMediaLibrarySharingDevices::get_Count, get_Count, get_Count method [Windows Media Library Sharing Services], get_Count method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevices interface, wmlss.IWMLSDevicesget_Count, wmlss/IWindowsMediaLibrarySharingDevices::get_Count
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
 - IWindowsMediaLibrarySharingDevices::get_Count
 - wmlss/IWindowsMediaLibrarySharingDevices::get_Count
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
 - IWindowsMediaLibrarySharingDevices.get_Count
---

# IWindowsMediaLibrarySharingDevices::get_Count


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Count</b> method retrieves the number of media devices on the home network.

## -parameters

### -param count [out]

A pointer to a <b>LONG</b> that receives the number of devices.

## -returns

This method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

