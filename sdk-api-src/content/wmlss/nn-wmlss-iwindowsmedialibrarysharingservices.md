---
UID: NN:wmlss.IWindowsMediaLibrarySharingServices
title: IWindowsMediaLibrarySharingServices (wmlss.h)
description: The IWindowsMediaLibrarySharingServices interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.
helpviewer_keywords: ["IWindowsMediaLibrarySharingServices","IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services]","described","wmlss.IWindowsMediaLibrarySharingServicesInterface","wmlss/IWindowsMediaLibrarySharingServices"]
old-location: wmlss\IWindowsMediaLibrarySharingServicesInterface.htm
tech.root: WMLSS
ms.assetid: bbec5687-3c77-4385-a9be-74c6d84db962
ms.date: 12/05/2018
ms.keywords: IWindowsMediaLibrarySharingServices, IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services], IWindowsMediaLibrarySharingServices interface [Windows Media Library Sharing Services],described, wmlss.IWindowsMediaLibrarySharingServicesInterface, wmlss/IWindowsMediaLibrarySharingServices
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
 - IWindowsMediaLibrarySharingServices
 - wmlss/IWindowsMediaLibrarySharingServices
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
 - IWindowsMediaLibrarySharingServices
---

# IWindowsMediaLibrarySharingServices interface


## -description

\[The feature associated with this page, [Windows Media Library Sharing Services](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). Media Casting has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use Media Casting instead of #FEATURENAMENOLINK#, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWindowsMediaLibrarySharingServices</b> interface defines methods that configure the sharing of media libraries among users on the local computer, users on the home network, and users on the Internet.

## -inheritance

The <b>IWindowsMediaLibrarySharingServices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWindowsMediaLibrarySharingServices</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain an <b>IWindowsMediaLibrarySharingServices</b> interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create a <b>WindowsMediaLibrarySharingServices</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
