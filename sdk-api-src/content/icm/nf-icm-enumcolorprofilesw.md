---
UID: NF:icm.EnumColorProfilesW
title: EnumColorProfilesW function
author: windows-sdk-content
description: The EnumColorProfiles function enumerates all the profiles satisfying the given enumeration criteria.
old-location: wcs\enumcolorprofiles.htm
tech.root: WCS
ms.assetid: 92d38155-e950-4c96-94e9-b66dbf090fca
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnumColorProfiles, EnumColorProfiles function [Windows Color System], EnumColorProfilesA, EnumColorProfilesW, _color_EnumColorProfiles, icm/EnumColorProfiles, icm/EnumColorProfilesA, icm/EnumColorProfilesW, wcs.enumcolorprofiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumColorProfilesW (Unicode) and EnumColorProfilesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - EnumColorProfiles
 - EnumColorProfilesA
 - EnumColorProfilesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumColorProfilesW function


## -description


The <b>EnumColorProfiles</b> function enumerates all the profiles satisfying the given enumeration criteria.


## -parameters




### -param pMachineName

Reserved. Must be <b>NULL</b>. This parameter is intended to point to the name of the computer on which to enumerate profiles. A <b>NULL</b> pointer indicates the local computer.


### -param pEnumRecord

Pointer to a structure specifying the enumeration criteria.


### -param pEnumerationBuffer

TBD


### -param pdwSizeOfEnumerationBuffer

TBD


### -param pnProfiles

Pointer to a variable that will contain, on return, the number of profile names actually copied to the buffer.


#### - pBuffer

Pointer to a buffer in which the profiles are to be enumerated. A MULTI_SZ string of profile names satisfying the criteria specified in <i>*pEnumRecord</i> will be placed in this buffer.


#### - pdwSize

Pointer to a variable containing the size of the buffer pointed to by <i>pBuffer</i>. On return, <i>*pdwSize</i> contains the size of buffer actually used or needed.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Several profiles are typically associated with printers, based on the paper and ink types. There is a default profile for each device. For International Color Consortium (ICC) profiles, GDI selects the best one from the ICC-associated profiles when your application creates a device context (DC).

Do not attempt to use <b>EnumColorProfiles</b> to determine the default profile for a device. Instead, create a device context for the device and then invoke the <a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a> function. On Windows Vista and Windows 7, the <a href="https://msdn.microsoft.com/a40ea9f3-ec56-459e-a55d-aad1b60ae7d4">WcsGetDefaultColorProfile</a> function can also be used to determine a device's default color profile.

If the <b>dwFields</b> member of the structure of type <b>ENUMTYPE</b> that is pointed to by the <i>pEnumRecord</i> parameter is set to ET_DEVICENAME, this function will enumerate all of the color profiles associated with all types of devices attached to the user's computer, regardless of the device class. If the <b>dwFields</b> member of the structure pointed to by the <i>pEnumRecord</i> parameter is set to ET_DEVICENAME or ET_DEVICECLASS and a device class is specified in the <b>dwDeviceClass</b> member of the structure, this function will only enumerate the profiles associated with the specified device class. If the <b>dwFields</b> member is set only to ET_DEVICECLASS, the <b>EnumColorProfiles</b> function will enumerate all profiles that can be associated with that type of device.

Whenever <b>EnumColorProfiles</b> is examining the profiles associated with a specific device, the results depend on whether the user has chosen to use the system-wide list of profiles associated with that device, or his or her own ("per-user") list. Calling <a href="https://msdn.microsoft.com/c108fbb2-e9f3-41fe-af36-99114df1507e">WcsSetUsePerUserProfiles</a> with its <i>usePerUserProfiles</i> parameter set to <b>TRUE</b> causes future calls to <b>EnumColorProfiles</b> to look at only the current user's per-user list of profile associations for the specified device. Calling <b>WcsSetUsePerUserProfiles</b> with its <i>usePerUserProfiles</i> parameter set to <b>FALSE</b> causes future calls to <b>EnumColorProfiles</b> to look at the system-wide list of profile associations for the specified device. If <b>WcsSetUsePerUserProfiles</b> has never been called for the current user, <b>EnumColorProfiles</b> examines the system-wide list.

Your application can use <b>EnumColorProfiles</b> to obtain the size of the buffer in which the profiles are enumerated. It should call the <b>EnumColorProfiles</b> function with the <i>pBuffer</i> parameter set to <b>NULL</b>. When the function returns, the <i>pdwSize</i> parameter will contain the required buffer size in bytes. Your program can use that information to allocate the enumeration buffer. It can then invoke <b>EnumColorProfiles</b> again with the <i>pBuffer</i> parameter set to the address of the buffer.

This function will provide the information for converting WCS-specific DMP information to the legacy EnumType record in enable consistent profile enumeration. The defaults will be the same as ICC if this information is not present.

<h3><a id="Per-user_LUA_support"></a><a id="per-user_lua_support"></a><a id="PER-USER_LUA_SUPPORT"></a>Per-user/LUA support</h3>
The enumeration is specific to current user. Both system wide and current user device associations are considered. For default profile configuration, current user settings override system wide ones.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/9c1065ad-00ac-4f5c-b738-090e38e1516f">ENUMTYPE</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/1e16771a-80c5-47bb-9c98-14169d4dd773">GetICMProfile</a>
 

 

