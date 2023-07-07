---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.put_Authorization
title: IWindowsMediaLibrarySharingDevice::put_Authorization (wmlss.h)
description: The put_Authorization method authorizes or unauthorizes the device to have access to the current user's media library.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services]","put_Authorization method","IWindowsMediaLibrarySharingDevice.put_Authorization","IWindowsMediaLibrarySharingDevice::put_Authorization","put_Authorization","put_Authorization method [Windows Media Library Sharing Services]","put_Authorization method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevice interface","wmlss.IWMLSDeviceput_Authorization","wmlss/IWindowsMediaLibrarySharingDevice::put_Authorization"]
old-location: wmlss\IWMLSDeviceput_Authorization.htm
tech.root: WMLSS
ms.assetid: 26ac8f24-d212-4558-a66e-ffe5e90bd73b
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],put_Authorization method, IWindowsMediaLibrarySharingDevice.put_Authorization, IWindowsMediaLibrarySharingDevice::put_Authorization, put_Authorization, put_Authorization method [Windows Media Library Sharing Services], put_Authorization method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceput_Authorization, wmlss/IWindowsMediaLibrarySharingDevice::put_Authorization
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
 - IWindowsMediaLibrarySharingDevice::put_Authorization
 - wmlss/IWindowsMediaLibrarySharingDevice::put_Authorization
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
 - IWindowsMediaLibrarySharingDevice.put_Authorization
---

# IWindowsMediaLibrarySharingDevice::put_Authorization


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_Authorization</b> method authorizes or unauthorizes the device to have access to the current user's media library.

## -parameters

### -param authorization [in]

An element of the <a href="/previous-versions/windows/desktop/api/wmlss/ne-wmlss-windowsmedialibrarysharingdeviceauthorizationstatus">WindowsMediaLibrarySharingDeviceAuthorizationStatus</a> enumeration that specifies whether the device is authorized (<b>DEVICE_AUTHORIZATION_ALLOWED</b>) or unauthorized (<b>DEVICE_AUTHORIZATION_DENIED</b>) to have access to the current user's media library.

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