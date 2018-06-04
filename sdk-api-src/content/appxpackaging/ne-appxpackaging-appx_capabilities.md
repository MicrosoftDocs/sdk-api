---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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




<a href="https://msdn.microsoft.com/5FCBD9E9-9A5E-49E1-8B80-8F84EDA8B07C">IAppxManifestReader::GetCapabilites</a>
 

 

