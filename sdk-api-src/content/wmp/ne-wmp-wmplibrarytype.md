---
UID: NE:wmp.WMPLibraryType
title: WMPLibraryType (wmp.h)
description: The WMPLibraryType enumeration type defines the possible library types to which Windows Media Player can connect.
helpviewer_keywords: ["WMPLibraryType","WMPLibraryType enumeration [Windows Media Player]","wmp.wmplibrarytype","wmp/WMPLibraryType","wmp/wmpltAll","wmp/wmpltDisc","wmp/wmpltLocal","wmp/wmpltPortableDevice","wmp/wmpltRemote","wmp/wmpltUnknown","wmpltAll","wmpltDisc","wmpltLocal","wmpltPortableDevice","wmpltRemote","wmpltUnknown"]
old-location: wmp\wmplibrarytype.htm
tech.root: WMP
ms.assetid: bf0e7140-5a33-4841-bd55-ac07dae09c41
ms.date: 12/05/2018
ms.keywords: WMPLibraryType, WMPLibraryType enumeration [Windows Media Player], wmp.wmplibrarytype, wmp/WMPLibraryType, wmp/wmpltAll, wmp/wmpltDisc, wmp/wmpltLocal, wmp/wmpltPortableDevice, wmp/wmpltRemote, wmp/wmpltUnknown, wmpltAll, wmpltDisc, wmpltLocal, wmpltPortableDevice, wmpltRemote, wmpltUnknown
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMPLibraryType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPLibraryType
 - wmp/WMPLibraryType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPLibraryType
---

# WMPLibraryType enumeration


## -description

The <b>WMPLibraryType</b> enumeration type defines the possible library types to which Windows Media Player can connect.

## -enum-fields

### -field wmpltUnknown:0

Not a valid library type.

### -field wmpltAll

All libraries.

### -field wmpltLocal

The current user's library.

### -field wmpltRemote

A library that belongs to another user on the same computer, the home network, or the Internet. The Player control must be running in remote mode to access these libraries. For information about running the Player control in remote mode, see <a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.

### -field wmpltDisc

Libraries on a data CD or DVD.

### -field wmpltPortableDevice

Libraries on portable devices.

## -remarks

Windows Media Player 10 Mobile: This enumeration is not supported.

## -see-also

<a href="/windows/desktop/WMP/about-library-services">About Library Services</a>



<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type">IWMPLibrary::get_type</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices">IWMPLibraryServices Interface</a>
