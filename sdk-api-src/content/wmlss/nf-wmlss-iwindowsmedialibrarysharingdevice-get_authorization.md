---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.get_Authorization
title: IWindowsMediaLibrarySharingDevice::get_Authorization (wmlss.h)
description: The get_Authorization method retrieves a value that indicates whether the device is authorized to have access to the current user's media library.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services]","get_Authorization method","IWindowsMediaLibrarySharingDevice.get_Authorization","IWindowsMediaLibrarySharingDevice::get_Authorization","get_Authorization","get_Authorization method [Windows Media Library Sharing Services]","get_Authorization method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevice interface","wmlss.IWMLSDeviceget_Authorization","wmlss/IWindowsMediaLibrarySharingDevice::get_Authorization"]
old-location: wmlss\IWMLSDeviceget_Authorization.htm
tech.root: WMLSS
ms.assetid: 0bdf06c4-f611-48c8-8289-e51351b234ee
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],get_Authorization method, IWindowsMediaLibrarySharingDevice.get_Authorization, IWindowsMediaLibrarySharingDevice::get_Authorization, get_Authorization, get_Authorization method [Windows Media Library Sharing Services], get_Authorization method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceget_Authorization, wmlss/IWindowsMediaLibrarySharingDevice::get_Authorization
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
 - IWindowsMediaLibrarySharingDevice::get_Authorization
 - wmlss/IWindowsMediaLibrarySharingDevice::get_Authorization
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
 - IWindowsMediaLibrarySharingDevice.get_Authorization
---

# IWindowsMediaLibrarySharingDevice::get_Authorization


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Authorization</b> method retrieves a value that indicates whether the device is  authorized to have access to the current user's media library.

## -parameters

### -param authorization [out]

A pointer to a variable that receives an element of the <a href="/previous-versions/windows/desktop/api/wmlss/ne-wmlss-windowsmedialibrarysharingdeviceauthorizationstatus">WindowsMediaLibrarySharingDeviceAuthorizationStatus</a> enumeration.

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