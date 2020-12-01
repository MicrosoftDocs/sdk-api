---
UID: NE:appxpackaging.APPX_CAPABILITIES
title: APPX_CAPABILITIES (appxpackaging.h)
description: Specifies the capabilities or privileges requested by a package.
helpviewer_keywords: ["APPX_CAPABILITIES","APPX_CAPABILITIES enumeration [App packaging and management]","APPX_CAPABILITY_DOCUMENTS_LIBRARY","APPX_CAPABILITY_ENTERPRISE_AUTHENTICATION","APPX_CAPABILITY_INTERNET_CLIENT","APPX_CAPABILITY_INTERNET_CLIENT_SERVER","APPX_CAPABILITY_MUSIC_LIBRARY","APPX_CAPABILITY_PICTURES_LIBRARY","APPX_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER","APPX_CAPABILITY_REMOVABLE_STORAGE","APPX_CAPABILITY_SHARED_USER_CERTIFICATES","APPX_CAPABILITY_VIDEOS_LIBRARY","appxpackaging/APPX_CAPABILITIES","appxpackaging/APPX_CAPABILITY_DOCUMENTS_LIBRARY","appxpackaging/APPX_CAPABILITY_ENTERPRISE_AUTHENTICATION","appxpackaging/APPX_CAPABILITY_INTERNET_CLIENT","appxpackaging/APPX_CAPABILITY_INTERNET_CLIENT_SERVER","appxpackaging/APPX_CAPABILITY_MUSIC_LIBRARY","appxpackaging/APPX_CAPABILITY_PICTURES_LIBRARY","appxpackaging/APPX_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER","appxpackaging/APPX_CAPABILITY_REMOVABLE_STORAGE","appxpackaging/APPX_CAPABILITY_SHARED_USER_CERTIFICATES","appxpackaging/APPX_CAPABILITY_VIDEOS_LIBRARY","appxpkg.appx_capabilities"]
old-location: appxpkg\appx_capabilities.htm
tech.root: appxpkg
ms.assetid: 4912BCB0-424B-40F9-BBD1-3AD0A60B3320
ms.date: 12/05/2018
ms.keywords: APPX_CAPABILITIES, APPX_CAPABILITIES enumeration [App packaging and management], APPX_CAPABILITY_DOCUMENTS_LIBRARY, APPX_CAPABILITY_ENTERPRISE_AUTHENTICATION, APPX_CAPABILITY_INTERNET_CLIENT, APPX_CAPABILITY_INTERNET_CLIENT_SERVER, APPX_CAPABILITY_MUSIC_LIBRARY, APPX_CAPABILITY_PICTURES_LIBRARY, APPX_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER, APPX_CAPABILITY_REMOVABLE_STORAGE, APPX_CAPABILITY_SHARED_USER_CERTIFICATES, APPX_CAPABILITY_VIDEOS_LIBRARY, appxpackaging/APPX_CAPABILITIES, appxpackaging/APPX_CAPABILITY_DOCUMENTS_LIBRARY, appxpackaging/APPX_CAPABILITY_ENTERPRISE_AUTHENTICATION, appxpackaging/APPX_CAPABILITY_INTERNET_CLIENT, appxpackaging/APPX_CAPABILITY_INTERNET_CLIENT_SERVER, appxpackaging/APPX_CAPABILITY_MUSIC_LIBRARY, appxpackaging/APPX_CAPABILITY_PICTURES_LIBRARY, appxpackaging/APPX_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER, appxpackaging/APPX_CAPABILITY_REMOVABLE_STORAGE, appxpackaging/APPX_CAPABILITY_SHARED_USER_CERTIFICATES, appxpackaging/APPX_CAPABILITY_VIDEOS_LIBRARY, appxpkg.appx_capabilities
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: APPX_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_CAPABILITIES
 - appxpackaging/APPX_CAPABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppxPackaging.h
api_name:
 - APPX_CAPABILITIES
---

# APPX_CAPABILITIES enumeration


## -description

Specifies the capabilities or privileges requested by a package.

## -enum-fields

### -field APPX_CAPABILITY_INTERNET_CLIENT

Your Internet connection for outgoing connections to the Internet.

### -field APPX_CAPABILITY_INTERNET_CLIENT_SERVER

Your Internet connection, including incoming unsolicited connections from the Internet – the app can send information to or from your computer through a firewall. You do not need to declare <b>APPX_CAPABILITY_INTERNET_CLIENT</b> if this capability is declared.

### -field APPX_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER

A home or work network – the app can send information to or from your computer and other computers on the same network.

### -field APPX_CAPABILITY_DOCUMENTS_LIBRARY

Your documents library, including the capability to add, change, or delete files. The package can access only file types that it has declared in the manifest. The app cannot access document libraries on HomeGroup computers.

### -field APPX_CAPABILITY_PICTURES_LIBRARY

Your pictures library, including the capability to add, change, or delete files. This capability also includes pictures libraries on HomeGroup computers, along with picture file types on locally connected media servers.

### -field APPX_CAPABILITY_VIDEOS_LIBRARY

Your videos library, including the capability to add, change, or delete files. This capability also includes videos libraries on HomeGroup computers, along with video file types on locally connected media servers.

### -field APPX_CAPABILITY_MUSIC_LIBRARY

Your music library and playlists, including the capability to add, change, or delete files. This capability also includes music libraries and playlists in the music library on HomeGroup computers, plus music file types on locally connected media servers.

### -field APPX_CAPABILITY_ENTERPRISE_AUTHENTICATION

Your Windows credentials, for access to a corporate intranet. This application can impersonate you on the network.

### -field APPX_CAPABILITY_SHARED_USER_CERTIFICATES

Software and hardware certificates or a smart card – used to identify you in the app. This capability may be used by your employer, bank, or government services to identify you.

### -field APPX_CAPABILITY_REMOVABLE_STORAGE

Removable storage, such as an external hard drive or USB flash drive, or MTP portable device, including the capability to add, change, or delete specific files. This package can only access file types that it has declared in the manifest.

### -field APPX_CAPABILITY_APPOINTMENTS

### -field APPX_CAPABILITY_CONTACTS

## -remarks

The <b>APPX_CAPABILITIES</b> enumeration specifies privileges that a package declares in the package manifest. If a capability is not explicitly declared, then the default is no access to that capability. If a capability is declared then  a package may still not have the particular capability for reasons such as the capability does not exist on the system or there are other security policies in place that limit the capability.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getcapabilities">IAppxManifestReader::GetCapabilites</a>