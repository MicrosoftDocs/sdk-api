---
UID: NS:winbase._COMMCONFIG
title: "_COMMCONFIG"
author: windows-sdk-content
description: Contains information about the configuration state of a communications device.
old-location: base\commconfig_str.htm
old-project: devio
ms.assetid: 9fd66f39-06a2-4159-9d1e-4ba84570c510
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*LPCOMMCONFIG, COMMCONFIG, COMMCONFIG structure, LPCOMMCONFIG, LPCOMMCONFIG structure pointer, _COMMCONFIG, _win32_commconfig_str, base.commconfig_str, winbase/COMMCONFIG, winbase/LPCOMMCONFIG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: COMMCONFIG, *LPCOMMCONFIG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - COMMCONFIG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

