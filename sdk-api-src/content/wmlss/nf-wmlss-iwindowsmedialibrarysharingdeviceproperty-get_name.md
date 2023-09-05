---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperty.get_Name
title: IWindowsMediaLibrarySharingDeviceProperty::get_Name (wmlss.h)
description: The get_Name method retrieves the name of an individual property of a media device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services]","get_Name method","IWindowsMediaLibrarySharingDeviceProperty.get_Name","IWindowsMediaLibrarySharingDeviceProperty::get_Name","get_Name","get_Name method [Windows Media Library Sharing Services]","get_Name method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDeviceProperty interface","wmlss.IWMLSDevicePropertyget_Name","wmlss/IWindowsMediaLibrarySharingDeviceProperty::get_Name"]
old-location: wmlss\IWMLSDevicePropertyget_Name.htm
tech.root: WMLSS
ms.assetid: 335e3beb-351e-40ad-b065-7058716180d3
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services],get_Name method, IWindowsMediaLibrarySharingDeviceProperty.get_Name, IWindowsMediaLibrarySharingDeviceProperty::get_Name, get_Name, get_Name method [Windows Media Library Sharing Services], get_Name method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperty interface, wmlss.IWMLSDevicePropertyget_Name, wmlss/IWindowsMediaLibrarySharingDeviceProperty::get_Name
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
 - IWindowsMediaLibrarySharingDeviceProperty::get_Name
 - wmlss/IWindowsMediaLibrarySharingDeviceProperty::get_Name
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
 - IWindowsMediaLibrarySharingDeviceProperty.get_Name
---

# IWindowsMediaLibrarySharingDeviceProperty::get_Name


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Name</b> method retrieves the name of an individual property of a media device.

## -parameters

### -param name [out]

A pointer to a <b>BSTR</b> that receives the property name.

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

