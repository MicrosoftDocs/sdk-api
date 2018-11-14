---
UID: NS:icm.tagPROFILE
title: tagPROFILE
author: windows-sdk-content
description: The PROFILE structure contains information that defines a color profile. See Using Device Profiles with WCS for more information.
old-location: wcs\profile.htm
tech.root: WCS
ms.assetid: e7f50d1a-3756-4da2-96ea-f9a5e1958be5
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PPROFILE, PROFILE, PROFILE structure [Windows Color System], _color_PROFILE_str, icm/PROFILE, tagPROFILE, wcs.profile"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Icm.h
api_name:
 - PROFILE
product: Windows
targetos: Windows
req.typenames: PROFILE
req.redist: 
---

# tagPROFILE structure


## -description



The <b>PROFILE</b> structure contains information that defines a color profile. See <a href="https://msdn.microsoft.com/9ea420ad-dcf1-4ba9-b739-308be7a56a6c">Using Device Profiles with WCS</a> for more information.




## -struct-fields




### -field dwType

Must be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PROFILE_FILENAME</td>
<td>Indicates that the <b>pProfileData</b> member contains a null-terminated string that holds the name of a device profile file.</td>
</tr>
<tr>
<td>PROFILE_MEMBUFFER</td>
<td>Indicates that the <b>pProfileData</b> member contains a pointer to a device profile in a memory buffer.</td>
</tr>
</table>
 


### -field pProfileData

The contents of this member is indicated by the <b>dwTYPE</b> member. It will either be a pointer to a null-terminated string containing the file name of the device profile, or it will be a pointer to a buffer in memory containing the device profile data.


### -field cbDataSize

The size in bytes of the data buffer pointed to by the <b>pProfileData</b> member.


## -see-also




<a href="https://msdn.microsoft.com/9ea420ad-dcf1-4ba9-b739-308be7a56a6c">Using Device Profiles with WCS</a>
 

 

