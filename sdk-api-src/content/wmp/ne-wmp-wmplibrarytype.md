---
UID: NE:wmp.WMPLibraryType
title: WMPLibraryType
author: windows-sdk-content
description: The WMPLibraryType enumeration type defines the possible library types to which Windows Media Player can connect.
old-location: wmp\wmplibrarytype.htm
tech.root: WMP
ms.assetid: bf0e7140-5a33-4841-bd55-ac07dae09c41
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMPLibraryType, WMPLibraryType enumeration [Windows Media Player], wmp.wmplibrarytype, wmp/WMPLibraryType, wmp/wmpltAll, wmp/wmpltDisc, wmp/wmpltLocal, wmp/wmpltPortableDevice, wmp/wmpltRemote, wmp/wmpltUnknown, wmpltAll, wmpltDisc, wmpltLocal, wmpltPortableDevice, wmpltRemote, wmpltUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: WMPLibraryType
req.redist: 
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



<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563394(v=VS.85).aspx">IWMPLibrary::get_type</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563384(v=VS.85).aspx">IWMPLibraryServices Interface</a>
 

 

