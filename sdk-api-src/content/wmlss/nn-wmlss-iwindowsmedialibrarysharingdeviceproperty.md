---
UID: NN:wmlss.IWindowsMediaLibrarySharingDeviceProperty
title: IWindowsMediaLibrarySharingDeviceProperty (wmlss.h)
description: The IWindowsMediaLibrarySharingDeviceProperty interface defines methods that provide access to the name and value of an individual property of a media device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDeviceProperty","IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services]","described","wmlss.IWindowsMediaLibrarySharingDevicePropertyInterface","wmlss/IWindowsMediaLibrarySharingDeviceProperty"]
old-location: wmlss\IWindowsMediaLibrarySharingDevicePropertyInterface.htm
tech.root: WMLSS
ms.assetid: 7b76cf66-0096-4b63-a30c-2df7d1a14527
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperty, IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperty interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicePropertyInterface, wmlss/IWindowsMediaLibrarySharingDeviceProperty
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
 - IWindowsMediaLibrarySharingDeviceProperty
 - wmlss/IWindowsMediaLibrarySharingDeviceProperty
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
 - IWindowsMediaLibrarySharingDeviceProperty
---

# IWindowsMediaLibrarySharingDeviceProperty interface


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface defines methods that provide access to the name and value of an individual property of a media device.

## -inheritance

The <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperty</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain an <b>IWindowsMediaLibrarySharingDeviceProperty</b> interface, call the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-getproperty">GetProperty</a> method or the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdeviceproperties-get_item">get_Item</a> method of the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdeviceproperties">IWindowsMediaLibrarySharingDeviceProperties</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
