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

# WMT_VERSION enumeration


## -description



The <b>WMT_VERSION</b> enumeration type defines the versions of the Windows Media Format SDK. Every profile you create will have an associated version identified by one of these enumerations. The version associated with a profile dictates the types of data allowed. For example, data unit extensions were introduced with version 8. A profile defined as version 7 cannot include data unit extensions. Under most circumstances, you will create profiles for the most current version.




## -enum-fields




### -field WMT_VER_4_0

Compatible with version 4 of the Windows Media Format SDK.


### -field WMT_VER_7_0

Compatible with the Windows Media Format 7 SDK.


### -field WMT_VER_8_0

Compatible with the Windows Media Format 8.2 SDK.


### -field WMT_VER_9_0

Compatible with the Windows Media Format 9 Series SDK, and with the Windows Media Format 9.5 SDK.


## -remarks



The version assigned to a profile does not directly relate to the codecs used in the profile's individual streams. However, it is recommended that you use codecs of the same version as the profile. Unless you have specific requirements to the contrary, you should always use the latest version.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

