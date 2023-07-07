---
UID: NF:wmlss.IWindowsMediaLibrarySharingDevice.get_Properties
title: IWindowsMediaLibrarySharingDevice::get_Properties (wmlss.h)
description: The get_Properties method retrieves an IWindowsMediaLibrarySharingDeviceProperties interface that represents the collection of all properties for the device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services]","get_Properties method","IWindowsMediaLibrarySharingDevice.get_Properties","IWindowsMediaLibrarySharingDevice::get_Properties","get_Properties","get_Properties method [Windows Media Library Sharing Services]","get_Properties method [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevice interface","wmlss.IWMLSDeviceget_Properties","wmlss/IWindowsMediaLibrarySharingDevice::get_Properties"]
old-location: wmlss\IWMLSDeviceget_Properties.htm
tech.root: WMLSS
ms.assetid: 771c102e-fa23-44bb-aa93-95f7ae9f5e36
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],get_Properties method, IWindowsMediaLibrarySharingDevice.get_Properties, IWindowsMediaLibrarySharingDevice::get_Properties, get_Properties, get_Properties method [Windows Media Library Sharing Services], get_Properties method [Windows Media Library Sharing Services],IWindowsMediaLibrarySharingDevice interface, wmlss.IWMLSDeviceget_Properties, wmlss/IWindowsMediaLibrarySharingDevice::get_Properties
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
 - IWindowsMediaLibrarySharingDevice::get_Properties
 - wmlss/IWindowsMediaLibrarySharingDevice::get_Properties
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
 - IWindowsMediaLibrarySharingDevice.get_Properties
---

# IWindowsMediaLibrarySharingDevice::get_Properties


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Properties</b> method retrieves an <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperties">IWindowsMediaLibrarySharingDeviceProperties</a> interface that represents the collection of all properties for the device.

## -parameters

### -param deviceProperties [out]

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperties">IWindowsMediaLibrarySharingDeviceProperties</a> interface.

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