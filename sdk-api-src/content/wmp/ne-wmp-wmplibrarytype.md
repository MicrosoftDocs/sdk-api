---
UID: NE:wmp.WMPLibraryType
title: WMPLibraryType
author: windows-sdk-content
description: The WMPLibraryType enumeration type defines the possible library types to which Windows Media Player can connect.
old-location: wmp\wmplibrarytype.htm
old-project: WMP
ms.assetid: bf0e7140-5a33-4841-bd55-ac07dae09c41
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WMPLibraryType, WMPLibraryType enumeration [Windows Media Player], wmp.wmplibrarytype, wmp/WMPLibraryType, wmp/wmpltAll, wmp/wmpltDisc, wmp/wmpltLocal, wmp/wmpltPortableDevice, wmp/wmpltRemote, wmp/wmpltUnknown, wmpltAll, wmpltDisc, wmpltLocal, wmpltPortableDevice, wmpltRemote, wmpltUnknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WMPLibraryType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPLibraryType
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMPLibraryType enumeration


## -description



The <b>WMPLibraryType</b> enumeration type defines the possible library types to which Windows Media Player can connect.




## -enum-fields




### -field wmpltUnknown

Not a valid library type.


### -field wmpltAll

All libraries.


### -field wmpltLocal

The current user's library.


### -field wmpltRemote

A library that belongs to another user on the same computer, the home network, or the Internet. The Player control must be running in remote mode to access these libraries. For information about running the Player control in remote mode, see <a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>.
            
          


### -field wmpltDisc

Libraries on a data CD or DVD.


### -field wmpltPortableDevice

Libraries on portable devices.


## -remarks



Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://msdn.microsoft.com/2334aa4a-7988-481d-9b21-9f7b432fbd05">About Library Services</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/95f36972-2227-4fe8-88d7-41f7aebbf67a">IWMPLibrary::get_type</a>



<a href="https://msdn.microsoft.com/9ed6d02e-15ca-425f-8642-e32a5adfaa55">IWMPLibraryServices Interface</a>
 

 

