---
UID: NF:wmlss.IWindowsMediaLibrarySharingServices.setDefaultAuthorization
title: IWindowsMediaLibrarySharingServices::setDefaultAuthorization (wmlss.h)
description: The setDefaultAuthorization method enables or disables access to all users' media libraries by a specified set of devices.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","setDefaultAuthorization method","IWindowsMediaLibrarySharingServices.setDefaultAuthorization","IWindowsMediaLibrarySharingServices::setDefaultAuthorization","setDefaultAuthorization","setDefaultAuthorization method [Windows Media Library Sharing Services]","setDefaultAuthorization method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface","wmlss.IWMLSSsetDefaultAuthorization","wmlss/IWindowsMediaLibrarySharingServices::setDefaultAuthorization"]
old-location: wmlss\IWMLSSsetDefaultAuthorization.htm
tech.root: WMLSS
ms.assetid: 7885f571-6b93-47d8-82ab-d998851f1304
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],setDefaultAuthorization method, IWindowsMediaLibrarySharingServices.setDefaultAuthorization, IWindowsMediaLibrarySharingServices::setDefaultAuthorization, setDefaultAuthorization, setDefaultAuthorization method [Windows Media Library Sharing Services], setDefaultAuthorization method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingServices interface, wmlss.IWMLSSsetDefaultAuthorization, wmlss/IWindowsMediaLibrarySharingServices::setDefaultAuthorization
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
 - IWindowsMediaLibrarySharingServices::setDefaultAuthorization
 - wmlss/IWindowsMediaLibrarySharingServices::setDefaultAuthorization
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
 - IWindowsMediaLibrarySharingServices.setDefaultAuthorization
---

# IWindowsMediaLibrarySharingServices::setDefaultAuthorization


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>setDefaultAuthorization</b> method enables or disables access to all users' media libraries by a specified set of devices.

## -parameters

### -param MACAddresses [in]

A <b>BSTR</b> that specifies the MAC addresses of the devices for which access will be enabled or disabled. The MAC addresses are delimited by commas.

### -param friendlyName [in]

A <b>BSTR</b> that specifies a friendly name that applies to all devices listed in the <i>MACAddresses</i> parameter.

### -param authorization [in]

A <b>VARIANT_BOOL</b> that specifies whether access by the set of devices is enabled (<b>VARIANT_TRUE</b>) or disabled (<b>VARIANT_FALSE</b>).

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

