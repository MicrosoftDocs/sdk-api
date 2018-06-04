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

# _COMMCONFIG structure


## -description


Contains information about the configuration state of a communications device.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. The caller must set this member to <code>sizeof(COMMCONFIG)</code>.


### -field wVersion

The version number of the structure. This parameter can be 1. The version of the provider-specific structure should be included in the <b>wcProviderData</b> member.


### -field wReserved

Reserved; do not use.


### -field dcb

The device-control block (<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>) structure for RS-232 serial devices. A 
<b>DCB</b> structure is always present regardless of the port driver subtype specified in the device's 
<a href="https://msdn.microsoft.com/d50ff606-1939-4e36-ba83-da8f269a3cc8">COMMPROP</a> structure.


### -field dwProviderSubType

The type of communications provider, and thus the format of the provider-specific data. For a list of communications provider types, see the description of the 
<a href="https://msdn.microsoft.com/d50ff606-1939-4e36-ba83-da8f269a3cc8">COMMPROP</a> structure.


### -field dwProviderOffset

The offset of the provider-specific data relative to the beginning of the structure, in bytes. This member is zero if there is no provider-specific data.


### -field dwProviderSize

The size of the provider-specific data, in bytes.


### -field wcProviderData

Optional provider-specific data. This member can be of any size or can be omitted. Because the 
<b>COMMCONFIG</b> structure may be expanded in the future, applications should use the <b>dwProviderOffset</b> member to determine the location of this member.


## -remarks



If the provider subtype is PST_RS232 or PST_PARALLELPORT, the <b>wcProviderData</b> member is omitted. If the provider subtype is PST_MODEM, the <b>wcProviderData</b> member contains a 
<a href="https://msdn.microsoft.com/4648992b-eeeb-4a8d-8e08-7e80f0dc56ef">MODEMSETTINGS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/d50ff606-1939-4e36-ba83-da8f269a3cc8">COMMPROP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>



<a href="https://msdn.microsoft.com/dbbf55d6-d369-4b28-bdc7-1fd9a736e658">GetCommProperties</a>



<a href="https://msdn.microsoft.com/4648992b-eeeb-4a8d-8e08-7e80f0dc56ef">MODEMSETTINGS</a>
 

 

