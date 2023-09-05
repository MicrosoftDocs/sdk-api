---
UID: NF:wmlss.IWindowsMediaLibrarySharingDeviceProperties.get_Item
title: IWindowsMediaLibrarySharingDeviceProperties::get_Item (wmlss.h)
description: The get_Item method retrieves an IWindowsMediaLibrarySharingDeviceProperty interface that represents an individual property for a media device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services]","get_Item method","IWindowsMediaLibrarySharingDeviceProperties.get_Item","IWindowsMediaLibrarySharingDeviceProperties::get_Item","get_Item","get_Item method [Windows Media Library Sharing Services]","get_Item method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDeviceProperties interface","wmlss.IWMLSDevicePropertiesget_Item","wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Item"]
old-location: wmlss\IWMLSDevicePropertiesget_Item.htm
tech.root: WMLSS
ms.assetid: 0c679f64-9d7e-4239-8ee0-2aa5de553c58
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],get_Item method, IWindowsMediaLibrarySharingDeviceProperties.get_Item, IWindowsMediaLibrarySharingDeviceProperties::get_Item, get_Item, get_Item method [Windows Media Library Sharing Services], get_Item method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDeviceProperties interface, wmlss.IWMLSDevicePropertiesget_Item, wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Item
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
 - IWindowsMediaLibrarySharingDeviceProperties::get_Item
 - wmlss/IWindowsMediaLibrarySharingDeviceProperties::get_Item
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
 - IWindowsMediaLibrarySharingDeviceProperties.get_Item
---

# IWindowsMediaLibrarySharingDeviceProperties::get_Item


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Item</b> method retrieves an <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperty">IWindowsMediaLibrarySharingDeviceProperty</a> interface that represents an individual property for a media device.

## -parameters

### -param index [in]

The zero-based index of the property in the collection of all properties associated with the media device.

### -param property [out]

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperty">IWindowsMediaLibrarySharingDeviceProperty</a> interface.

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