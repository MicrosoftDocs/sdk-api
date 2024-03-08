---
UID: NN:wmlss.IWindowsMediaLibrarySharingDevice
title: IWindowsMediaLibrarySharingDevice (wmlss.h)
description: The IWindowsMediaLibrarySharingDevice interface defines methods that provide access to an individual media device on the home network.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDevice","IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services]","described","wmlss.IWindowsMediaLibrarySharingDeviceInterface","wmlss/IWindowsMediaLibrarySharingDevice"]
old-location: wmlss\IWindowsMediaLibrarySharingDeviceInterface.htm
tech.root: WMLSS
ms.assetid: 33fe649b-a688-435c-a019-9c308935532e
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDevice, IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDevice interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDeviceInterface, wmlss/IWindowsMediaLibrarySharingDevice
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
 - IWindowsMediaLibrarySharingDevice
 - wmlss/IWindowsMediaLibrarySharingDevice
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
 - IWindowsMediaLibrarySharingDevice
---

# IWindowsMediaLibrarySharingDevice interface


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWindowsMediaLibrarySharingDevice</b> interface defines methods that provide access to an individual media device on the home network.

## -inheritance

The <b>IWindowsMediaLibrarySharingDevice</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDevice</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain an <b>IWindowsMediaLibrarySharingDevice</b> interface, call the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-getdevice">GetDevice</a> method or the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevices-get_item">get_Item</a> method of the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevices">IWindowsMediaLibrarySharingDevices</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
