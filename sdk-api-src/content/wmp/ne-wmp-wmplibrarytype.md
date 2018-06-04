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
 

 

