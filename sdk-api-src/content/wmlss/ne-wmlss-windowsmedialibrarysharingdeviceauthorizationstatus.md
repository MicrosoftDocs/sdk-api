---
UID: NE:wmlss.WindowsMediaLibrarySharingDeviceAuthorizationStatus
title: WindowsMediaLibrarySharingDeviceAuthorizationStatus (wmlss.h)
description: The WindowsMediaLibrarySharingDeviceAuthorizationStatus enumeration defines constants that indicate whether a media device is authorized to have access to a media library.
helpviewer_keywords: ["DEVICE_AUTHORIZATION_ALLOWED","DEVICE_AUTHORIZATION_DENIED","DEVICE_AUTHORIZATION_UNKNOWN","WindowsMediaLibrarySharingDeviceAuthorizationStatus","WindowsMediaLibrarySharingDeviceAuthorizationStatus enumeration [Windows Media Library Sharing Services]","wmlss.WMLSDeviceAuthorizationStatusEnumeration","wmlss/DEVICE_AUTHORIZATION_ALLOWED","wmlss/DEVICE_AUTHORIZATION_DENIED","wmlss/DEVICE_AUTHORIZATION_UNKNOWN","wmlss/WindowsMediaLibrarySharingDeviceAuthorizationStatus"]
old-location: wmlss\WMLSDeviceAuthorizationStatusEnumeration.htm
tech.root: WMLSS
ms.assetid: 2b858236-32d9-410e-bf57-207a1c44c9d5
ms.date: 12/05/2018
ms.keywords: DEVICE_AUTHORIZATION_ALLOWED, DEVICE_AUTHORIZATION_DENIED, DEVICE_AUTHORIZATION_UNKNOWN, WindowsMediaLibrarySharingDeviceAuthorizationStatus, WindowsMediaLibrarySharingDeviceAuthorizationStatus enumeration [Windows Media Library Sharing Services], wmlss.WMLSDeviceAuthorizationStatusEnumeration, wmlss/DEVICE_AUTHORIZATION_ALLOWED, wmlss/DEVICE_AUTHORIZATION_DENIED, wmlss/DEVICE_AUTHORIZATION_UNKNOWN, wmlss/WindowsMediaLibrarySharingDeviceAuthorizationStatus
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsMediaLibrarySharingDeviceAuthorizationStatus
 - wmlss/WindowsMediaLibrarySharingDeviceAuthorizationStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmlss.h
api_name:
 - WindowsMediaLibrarySharingDeviceAuthorizationStatus
---

# WindowsMediaLibrarySharingDeviceAuthorizationStatus enumeration


## -description

The <b>WindowsMediaLibrarySharingDeviceAuthorizationStatus</b> enumeration defines constants that indicate whether a media device is authorized to have access to a media library.

## -enum-fields

### -field DEVICE_AUTHORIZATION_UNKNOWN:0

It is not known whether the device is authorized to have access to the media library.

### -field DEVICE_AUTHORIZATION_ALLOWED:1

The device is authorized to have access to the media library.

### -field DEVICE_AUTHORIZATION_DENIED:2

The device is not authorized to have access to the media library.

## -see-also

<a href="/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal">Windows Media Library Sharing Services</a>
