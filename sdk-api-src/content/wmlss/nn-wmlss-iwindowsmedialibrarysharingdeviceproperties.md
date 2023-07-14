---
UID: NN:wmlss.IWindowsMediaLibrarySharingDeviceProperties
title: IWindowsMediaLibrarySharingDeviceProperties (wmlss.h)
description: The IWindowsMediaLibrarySharingDeviceProperties interface defines methods that provide access to the collection of all properties for an individual media device.
helpviewer_keywords: ["IWindowsMediaLibrarySharingDeviceProperties","IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services]","described","wmlss.IWindowsMediaLibrarySharingDevicePropertiesInterface","wmlss/IWindowsMediaLibrarySharingDeviceProperties"]
old-location: wmlss\IWindowsMediaLibrarySharingDevicePropertiesInterface.htm
tech.root: WMLSS
ms.assetid: b975428c-e518-4bc8-a621-193d510661b0
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingDeviceProperties, IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingDeviceProperties interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingDevicePropertiesInterface, wmlss/IWindowsMediaLibrarySharingDeviceProperties
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
 - IWindowsMediaLibrarySharingDeviceProperties
 - wmlss/IWindowsMediaLibrarySharingDeviceProperties
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
 - IWindowsMediaLibrarySharingDeviceProperties
---

# IWindowsMediaLibrarySharingDeviceProperties interface


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface defines methods that provide access to the collection of all properties for an individual media device.

## -inheritance

The <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingDeviceProperties</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain an <b>IWindowsMediaLibrarySharingDeviceProperties</b> interface, call the <a href="/previous-versions/windows/desktop/api/wmlss/nf-wmlss-iwindowsmedialibrarysharingdevice-get_properties">get_Properties</a> method of the <a href="/previous-versions/windows/desktop/api/wmlss/nn-wmlss-iwindowsmedialibrarysharingdevice">IWindowsMediaLibrarySharingDevice</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
