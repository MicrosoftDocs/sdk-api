---
UID: NS:winbase.tagHW_PROFILE_INFOW
title: HW_PROFILE_INFOW (winbase.h)
description: Contains information about a hardware profile. (Unicode)
helpviewer_keywords: ["*LPHW_PROFILE_INFOW","DOCKINFO_DOCKED","DOCKINFO_UNDOCKED","DOCKINFO_USER_DOCKED","DOCKINFO_USER_SUPPLIED","DOCKINFO_USER_UNDOCKED","HW_PROFILE_INFO","HW_PROFILE_INFO structure","HW_PROFILE_INFOA","HW_PROFILE_INFOW","LPHW_PROFILE_INFO","LPHW_PROFILE_INFO structure pointer","_win32_hw_profile_info_str","base.hw_profile_info_str","tagHW_PROFILE_INFOA","tagHW_PROFILE_INFOW","winbase/HW_PROFILE_INFO","winbase/HW_PROFILE_INFOA","winbase/HW_PROFILE_INFOW","winbase/LPHW_PROFILE_INFO"]
old-location: base\hw_profile_info_str.htm
tech.root: winprog
ms.assetid: b1c8eb4c-8c62-4e3e-a7d2-0888512b3d4c
ms.date: 12/05/2018
ms.keywords: '*LPHW_PROFILE_INFOW, DOCKINFO_DOCKED, DOCKINFO_UNDOCKED, DOCKINFO_USER_DOCKED, DOCKINFO_USER_SUPPLIED, DOCKINFO_USER_UNDOCKED, HW_PROFILE_INFO, HW_PROFILE_INFO structure, HW_PROFILE_INFOA, HW_PROFILE_INFOW, LPHW_PROFILE_INFO, LPHW_PROFILE_INFO structure pointer, _win32_hw_profile_info_str, base.hw_profile_info_str, tagHW_PROFILE_INFOA, tagHW_PROFILE_INFOW, winbase/HW_PROFILE_INFO, winbase/HW_PROFILE_INFOA, winbase/HW_PROFILE_INFOW, winbase/LPHW_PROFILE_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: HW_PROFILE_INFOW (Unicode) and HW_PROFILE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HW_PROFILE_INFOW, *LPHW_PROFILE_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHW_PROFILE_INFOW
 - winbase/tagHW_PROFILE_INFOW
 - LPHW_PROFILE_INFOW
 - winbase/LPHW_PROFILE_INFOW
 - HW_PROFILE_INFOW
 - winbase/HW_PROFILE_INFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - HW_PROFILE_INFO
 - HW_PROFILE_INFOA
 - HW_PROFILE_INFOW
---

# HW_PROFILE_INFOW structure


## -description

Contains information about a hardware profile. The 
<a href="/windows/desktop/api/winbase/nf-winbase-getcurrenthwprofilea">GetCurrentHwProfile</a> function uses this structure to retrieve the current hardware profile for the local computer.

## -struct-fields

### -field dwDockInfo

The reported docking state of the computer. This member can be a combination of the following bit values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_DOCKED"></a><a id="dockinfo_docked"></a><dl>
<dt><b>DOCKINFO_DOCKED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The computer is docked. 

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_UNDOCKED"></a><a id="dockinfo_undocked"></a><dl>
<dt><b>DOCKINFO_UNDOCKED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The computer is undocked. This flag is always set for desktop systems that cannot be undocked.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_SUPPLIED"></a><a id="dockinfo_user_supplied"></a><dl>
<dt><b>DOCKINFO_USER_SUPPLIED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
If this flag is set, 
<a href="/windows/desktop/api/winbase/nf-winbase-getcurrenthwprofilea">GetCurrentHwProfile</a> retrieved the current docking state from information provided by the user in the <b>Hardware Profiles</b> page of the <b>System</b> control panel application. 




If there is no such value or the value is set to 0, this flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_DOCKED"></a><a id="dockinfo_user_docked"></a><dl>
<dt><b>DOCKINFO_USER_DOCKED</b></dt>
<dt>0x5</dt>
</dl>
</td>
<td width="60%">
The computer is docked, according to information provided by the user. This value is a combination of the DOCKINFO_USER_SUPPLIED and DOCKINFO_DOCKED flags.

</td>
</tr>
<tr>
<td width="40%"><a id="DOCKINFO_USER_UNDOCKED"></a><a id="dockinfo_user_undocked"></a><dl>
<dt><b>DOCKINFO_USER_UNDOCKED</b></dt>
<dt>0x6</dt>
</dl>
</td>
<td width="60%">
The computer is undocked, according to information provided by the user. This value is a combination of the DOCKINFO_USER_SUPPLIED and DOCKINFO_UNDOCKED flags.

</td>
</tr>
</table>

### -field szHwProfileGuid

The globally unique identifier (GUID) string for the current hardware profile. The string returned by 
<a href="/windows/desktop/api/winbase/nf-winbase-getcurrenthwprofilea">GetCurrentHwProfile</a> encloses the GUID in curly braces, {}; for example: 




{12340001-4980-1920-6788-123456789012}

You can use this string as a registry subkey under your application's configuration settings key in <b>HKEY_CURRENT_USER</b>. This enables you to store settings for each hardware profile.

### -field szHwProfileName

The display name for the current hardware profile.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getcurrenthwprofilea">GetCurrentHwProfile</a>

## -remarks

> [!NOTE]
> The winbase.h header defines HW_PROFILE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
